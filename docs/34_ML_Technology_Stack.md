## Technical components

#### 0. High level architecture : 
--------------
```
version 0.1 :
   - have 'python tutor real time editor' and 'Google TTS based Lesson teaching' as separate systems . Reasons a) quick implementation b) we can think how to integrate once 2 pieces are working
   
  python tutor:
    - follow install of v5-unity
    - comment out ( or remove) the other text on the main screen
    
  TTS Lessons:
     - find that black scrren editor ACE editor notes by searching OUR repo
     - have  Django & Mobx as components . Mobx gives simplicity so no 'DidComponentMount' etc.. nonsense of React js
     - Django : have simple Django & React as shown below, replace React with Mobx . Django-cookie-cutter is later versoions 
     - use Sqllite DB , PostgreSql later
     - use Github, later Atlasian BitBucket
     
```

#### 1. Django & Mobx/React Setup : 
--------------

- start with this  Django + React stack 
https://wsvincent.com/django-rest-framework-react-tutorial/


This project is heavily inspired by cookiecutter-django. If you're looking for an even more advanced framework that comes with deployment configurations, give it a look!

cookie cutter django https://github.com/pydanny/cookiecutter-django


- All Articles : https://wsvincent.com/django-best-practices/

https://wsvincent.com/django-rest-framework-user-authentication-tutorial/

https://wsvincent.com/django-rest-framework-authentication-tutorial/

https://wsvincent.com/django-best-practices/


#### 3. Python Tutor : 
--------------
- so many people helped/advised [from Security & other perspecives](https://github.com/pgbovine/OnlinePythonTutor) : Peter Norvig, Guido van Rossum so truasure this because it is the BEST LEARNING Experience solicited from so many people 
- v5-Unity [Developer notes ](https://github.com/pgbovine/OnlinePythonTutor/blob/master/v5-unity/README.txt) 
```
UPDATE: it was tested on 2018-05-26 with:

$ webpack -v
3.11.0

$ tsc -v
Version 2.8.3
```
