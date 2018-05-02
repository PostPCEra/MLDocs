---
id: 16_DevOps
title: DevOps = IT Automation
sidebar_label: DevOps = Continual Experimentation
---


## 1. Provisioning & Conig. management

### 1.1 The 15-point DevOps Check List

> Culture Of [Continual Experimentation And Learning](https://medium.com/devopslinks/the-15-point-devops-check-list-8cd2afb4a448)

- Shorter Development Cycles & Time-To-Market
- Time-to-market (TTM) is the length of time it takes from the conception stage to the product being deployed and running in production servers.
 
| Topic           | Notes | 
| --------------- | ------|
| config in VCS | You system configuration should be always into a source control service/servers| 
| Prod-like systems | Developers should be able to create systems with production-like configurations and data| 
| Dev access to CI | Developers should have access to continuous integration tasks to build softwares and test artifacts in a short period: I prefer working with git hooks, where an automatic build is launched right when a developer push a change to development branch| 

- Key Performance Indicators KPI : Department level
- The DevOps Feedback Loop
- Automating measurements

### 1.2 Ansible


| Title | What | Notes | 
| ------- | -----| ----  | 
| Ansible begginer 5 videos| great hands-on | [youtube](https://www.youtube.com/channel/UCLLumGsi1QboyiFIJf8a-0w)
| Ansible slide deck | read  basics | [slides](https://www.slideshare.net/GulcinYildirim/managing-postgresql-with-ansible-fosdem-pgday-2016)
| Simple Ansible Playbook | helps learn Ansible basics | [github](https://github.com/myarik/django-ansible-setup)   | 
| Automating Django Deployments with Fabric and Ansible | -----| [article](https://realpython.com/automating-django-deployments-with-fabric-and-ansible/)
| Ansible Playbook for setting up a Djang | Full blown| [gold standard](https://github.com/jcalazan/ansible-django-stack)  | 

first try with item #1 to understand fundamentals of Ansible , then finally #3

So how can I use Ansible?
> In the simplest form, you need three components: an Ansible server, remote hosts and a playbook.

![Ansible1](/docs/assets/Ansible-with-IT.jpg)
![Why Ansible?](/docs/assets/why-ansible.jpg)
![Ansible1](/docs/assets/Ansible-BBlocks.png)
![Ansible1](/docs/assets/Ansible1.png)
![Ansible2](/docs/assets/Ansible2.png)


### 1.3 Docker

Docker notes goes here .....

| Title   |  Note  | Notes | 
| ------- |  ----  | ------ |
|Learn Docker in 12 Minutes | | [best](https://www.youtube.com/watch?v=YFl2mCHdv24&t=366s) 3/17|
|Docker Compose in 12 Minuts |[github](https://github.com/jakewright/tutorials/tree/master/docker/02-docker-compose) | [love](https://www.youtube.com/watch?v=Qw9zlE3t8Ko) 3/17|
|From Zero to Docker - Tutorial for Beginner | | [Theory](https://www.youtube.com/watch?v=JprTjTViaEA&t=139s) 6/17 |
|Deploying Django web applications in Docker containers | | [youtube](https://www.youtube.com/watch?v=T2hooQzvurQ) 10/17 |
|Dockerizing a Django REST Framework Project | |  [youtube](https://www.youtube.com/watch?v=Y_rh-VeC_j4) 8/17 |
|Building Python apps with Docker | |[youtube](https://www.youtube.com/watch?v=VhabrYF1nms&t=20s)|

[Jake](https://www.youtube.com/watch?v=AMqkTIs-ngQ) - Cambridge Comp. Sc grad of above Docker 12 min.

## 2. CI & CD

> Unlike compiled languages, [Python doesn’t need a "build" per se](https://jenkins.io/solutions/python/). 
Python projects can still benefit greatly from using Jenkins for continuous integration and delivery.


Except Java and C, other Languages doesn't have `Build` per se. The list goes on Python/PHP/Ruby, Javascript ... That is the reason `Jenkins` origions are so much JAVA Build system centered .
 
An [Introduction to CI/CD Best Practices](https://www.digitalocean.com/community/tutorials/an-introduction-to-ci-cd-best-practices)
 
### 2.1 Jenkins

Configuring a [Jenkins Pipeline using a YAML file ](https://jenkins.io/blog/2018/04/25/configuring-jenkins-pipeline-with-yaml-file/)
 - the above is experimental, but shows promise of Jenkin config coming to YMAL 


### 2.2 BuildBot

After Jenkin, python based CI Server [BuildBot]() is popular [as per this](https://blog.taiga.io/6-excellent-continuous-integration-tools.html).

`BuildBot` is used by `Mozilla, Webkit, Chromium`

| Title   |  Notes | 
| ------- |  ----  | 
| How To Set Up Continuous Integration with Buildbot on Ubuntu 16.04 | [Digital ocean](https://www.digitalocean.com/community/tutorials/how-to-set-up-continuous-integration-with-buildbot-on-ubuntu-16-04) |
| | |

`Conclusion : `
In this tutorial, we configured Buildbot to listen for changes to a GitHub repository using webhooks. When a change is received, Buildbot starts up a container based on a custom Docker image to test the new commit. The Docker image contains a Buildbot worker instance as well as the dependencies needed to test our project code. This allows Buildbot to dynamically start Buildbot workers as needed whenever a change is made to the repository.
 
  
### 2.3 hosted CI tool vendors 
  Circle CI, Travis CI 


[DevOps Toolbox](https://hostadvice.com/blog/devops-toolbox-jenkins-ansible-chef-puppet-vagrant-saltstack/) - some good tools parts showing Jenkins can integrate all CI/CD Ecosystem ( some of that integration may be only available in CloudBees not in FOSS Jenkins), but CI coluld host vendors `Travis CI` `Circle CI` etc are 
missing. It seems this post is promoting more of sponsers of the website like CloudBee (Enterprise Jenkins) etc..


## 3. Version Control System VCS

### 3.1 Bitbucket , github