---
id: 351_OnlineJudge
title: OnlineJudge 2.0
sidebar_label: Online Judge
---


**An onlinejudge system based on Python and Vue.** 

`Python ` 3.6  <br>
`Django ` 1.11.4  <br>
`Django Rest Framework ` 3.4.0   

[The Other Django Docker project](https://github.com/raymestalez/django-react-blog)
 - give it as first try
 - it is trying to install ubantu and failed ..

## Overview
- Based on Docker; One-click deployment
- Separated backend and frontend; Modular programming; Micro service
- ACM/OI rule support; realtime/non-realtime rank support
- Amazing charting and visualization
- Template-problem support
- More reasonable permission control
- Multi-language support: C, C++, Java, Python2, Python3
- Markdown & MathJax support
- Contest participants IP limit(CIDR)


**Main modules are available below:**

- Backend(Django): https://github.com/QingdaoU/OnlineJudge
- Frontend(Vue): https://github.com/QingdaoU/OnlineJudgeFE
- Judger Sandbox(Seccomp): https://github.com/QingdaoU/Judger
- JudgeServer(A wrapper for Judger): https://github.com/QingdaoU/JudgeServer

**Installation** : https://github.com/QingdaoU/OnlineJudgeDeploy/tree/2.0

**Documentation** :http://docs.onlinejudge.me/


## CODE 


### Quality metrics
- Docker-compose based installation 
- Separate VENDOR_APPS and LOCAL_APPS, this shows the `quality of the project `  INSTALLED_APPS = VENDOR_APPS + LOCAL_APPS
-  `utils ` is a separate microservice App
- AUTH_USER_MODEL = 'account.User' ( account is microervice app)
- TEST_CASE_DIR  for holding test cases
- Logging, Loggers
- Redis, Celeary integration 


### [oj/settings.py](https://github.com/QingdaoU/OnlineJudge/blob/master/oj/settings.py)
```python

production_env = get_env("OJ_ENV", "dev") == "production"
if production_env:
    from .production_settings import *
else:
    from .dev_settings import *

BASE_DIR = os.path.dirname(os.path.dirname(os.path.abspath(__file__)))

# Applications
VENDOR_APPS = (
    'django.contrib.auth',
    'django.contrib.sessions',
    'django.contrib.contenttypes',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'rest_framework',
    'raven.contrib.django.raven_compat'
)
LOCAL_APPS = (
    'account',
    'announcement',
    'conf',
    'problem',
    'contest',
    'utils',
    'submission',
    'options',
    'judge',
)

INSTALLED_APPS = VENDOR_APPS + LOCAL_APPS

MIDDLEWARE_CLASSES = (
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    # 'account.middleware.LogSqlMiddleware',
)
ROOT_URLCONF = 'oj.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
WSGI_APPLICATION = 'oj.wsgi.application'

# Password validation
# https://docs.djangoproject.com/en/1.9/ref/settings/#auth-password-validators

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
]

# Internationalization
# https://docs.djangoproject.com/en/1.8/topics/i18n/

LANGUAGE_CODE = 'en-us'

TIME_ZONE = 'UTC'

USE_I18N = True

USE_L10N = True

USE_TZ = True

# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/1.8/howto/static-files/

STATIC_URL = '/public/'

AUTH_USER_MODEL = 'account.User'

TEST_CASE_DIR = os.path.join(DATA_DIR, "test_case")
LOG_PATH = os.path.join(DATA_DIR, "log")

AVATAR_URI_PREFIX = "/public/avatar"
AVATAR_UPLOAD_DIR = f"{DATA_DIR}{AVATAR_URI_PREFIX}"

UPLOAD_PREFIX = "/public/upload"
UPLOAD_DIR = f"{DATA_DIR}{UPLOAD_PREFIX}"

STATICFILES_DIRS = [os.path.join(DATA_DIR, "public")]


LOGGING_HANDLERS = ['console', 'sentry'] if production_env else ['console']
LOGGING = {
   'version': 1,
   'disable_existing_loggers': False,
   'formatters': {
       'standard': {
           'format': '[%(asctime)s] - [%(levelname)s] - [%(name)s:%(lineno)d]  - %(message)s',
           'datefmt': '%Y-%m-%d %H:%M:%S'
       }
   },
   'handlers': {
       'console': {
           'level': 'DEBUG',
           'class': 'logging.StreamHandler',
           'formatter': 'standard'
       },
       'sentry': {
           'level': 'ERROR',
           'class': 'raven.contrib.django.raven_compat.handlers.SentryHandler',
           'formatter': 'standard'
       }
   },
   'loggers': {
       'django.request': {
           'handlers': LOGGING_HANDLERS,
           'level': 'ERROR',
           'propagate': True,
       },
       'django.db.backends': {
           'handlers': LOGGING_HANDLERS,
           'level': 'ERROR',
           'propagate': True,
       },
       '': {
           'handlers': LOGGING_HANDLERS,
           'level': 'WARNING',
           'propagate': True,
       }
   },
}

REST_FRAMEWORK = {
    'TEST_REQUEST_DEFAULT_FORMAT': 'json',
    'DEFAULT_RENDERER_CLASSES': (
        'rest_framework.renderers.JSONRenderer',
    )
}

REDIS_URL = "redis://%s:%s" % (REDIS_CONF["host"], REDIS_CONF["port"])


def redis_config(db):
    def make_key(key, key_prefix, version):
        return key

    return {
        "BACKEND": "utils.cache.MyRedisCache",
        "LOCATION": f"{REDIS_URL}/{db}",
        "TIMEOUT": None,
        "KEY_PREFIX": "",
        "KEY_FUNCTION": make_key
    }


CACHES = {
    "default": redis_config(db=1)
}

SESSION_ENGINE = "django.contrib.sessions.backends.cache"
SESSION_CACHE_ALIAS = "default"

CELERY_RESULT_BACKEND = f"{REDIS_URL}/2"
BROKER_URL = f"{REDIS_URL}/3"
CELERY_TASK_SOFT_TIME_LIMIT = CELERY_TASK_TIME_LIMIT = 180
CELERY_ACCEPT_CONTENT = ["json"]
CELERY_TASK_SERIALIZER = "json"
RAVEN_CONFIG = {
    'dsn': 'https://b200023b8aed4d708fb593c5e0a6ad3d:1fddaba168f84fcf97e0d549faaeaff0@sentry.io/263057'
}

IP_HEADER = "HTTP_X_REAL_IP"
```

### [utils/constants.py](https://github.com/QingdaoU/OnlineJudge/blob/master/utils/constants.py)

```python
class Choices:
    @classmethod
    def choices(cls):
        d = cls.__dict__
        return [d[item] for item in d.keys() if not item.startswith("__")]


class ContestType:
    PUBLIC_CONTEST = "Public"
    PASSWORD_PROTECTED_CONTEST = "Password Protected"


class ContestStatus:
    CONTEST_NOT_START = "1"
    CONTEST_ENDED = "-1"
    CONTEST_UNDERWAY = "0"


class ContestRuleType(Choices):
    ACM  =  " ACM "
    OI = "OI"


class CacheKey:
    waiting_queue = "waiting_queue"
    contest_rank_cache = "contest_rank_cache"
    website_config = "website_config"
    option = "option"


class Difficulty(Choices):
    LOW = "Low"
    MID = "Mid"
    HIGH = "High"
```


### docker-compose install

`Prepare installation files`

git clone -b 2.0 https://github.com/QingdaoU/OnlineJudgeDeploy.git && cd OnlineJudgeDeploy


`Start the service`

docker-compose up -d

[docker-compose .yml](https://github.com/QingdaoU/OnlineJudgeDeploy)

```yml
version: "3"
services:

  oj-redis:
    image: registry.docker-cn.com/library/redis:4.0-alpine
    container_name: oj-redis
    restart: always
    volumes:
      - $PWD/data/redis:/data
  
  oj-postgres:
    image: registry.docker-cn.com/library/postgres:10-alpine
    container_name: oj-postgres
    restart: always
    volumes:
      - $PWD/data/postgres:/var/lib/postgresql/data
    environment:
      - POSTGRES_DB=onlinejudge
      - POSTGRES_USER=onlinejudge
      - POSTGRES_PASSWORD=onlinejudge

  judge-server:
    image: registry.cn-hangzhou.aliyuncs.com/onlinejudge/judge_server
    container_name: judge-server
    restart: always
    read_only: true
    cap_drop:
      - SETPCAP
      - MKNOD
      - NET_BIND_SERVICE
      - SYS_CHROOT
      - SETFCAP
      - FSETID
    tmpfs:
      - /tmp
      - /judger_run:exec,mode=777
      - /spj:exec,mode=777
      # - /dev/shm:mode=777
    volumes:
      - $PWD/data/backend/test_case:/test_case:ro
      - $PWD/data/judge_server:/log
    environment:
      - SERVICE_URL=http://judge-server:8080
      - BACKEND_URL=http://oj-backend:8000/api/judge_server_heartbeat/
      - TOKEN=CHANGE_THIS
  
  oj-backend:
    image: registry.cn-hangzhou.aliyuncs.com/onlinejudge/oj_backend
    container_name: oj-backend
    restart: always
    depends_on:
      - oj-redis
      - oj-postgres
      - judge-server
    volumes:
      - $PWD/data/backend:/data
    environment:
      - POSTGRES_DB=onlinejudge
      - POSTGRES_USER=onlinejudge
      - POSTGRES_PASSWORD=onlinejudge
      - JUDGE_SERVER_TOKEN=CHANGE_THIS
      # - FORCE_HTTPS=1
      # - STATIC_CDN_HOST=cdn.oj.com
    ports:
      - "0.0.0.0:80:8000"
      - "0.0.0.0:443:1443"
```



