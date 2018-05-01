---
id: 16_DevOps
title: DevOps = IT Automation
sidebar_label: DevOps = IT Automation
---


## 1. Provisioning & Conig. management

### The 15-point DevOps Check List

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

### Ansible


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


### Docker

Docker notes goes here .....


## 2. CI & CD

Noticed many companies using Jenkins as CI tool 
 
### Jenkins

### hosted CI tool vendors 
  Circle CI, Travis CI 


## 3. Version Control System VCS

### Bitbucket , github