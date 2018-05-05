---
id: 31_ML_building_business
title: ML building business
sidebar_label: ML building business
---

## Mastery Learn

### What problems we r solving

### How ? w/ unique Pedagogy



## Building Business

### Business Models

**Models**


| Company | Date | Notes |
| ------- | -----| ----  | 
| Lambda  | -----| 6 months, 17% for 24 months ; get material from other Place  | 
| [Recurse](https://www.recurse.com/blog/131-join-rc-and-help-grow-a-new-kind-of-business-and-community) | 2/2018  | 1. Experienced & new programmers come to RC from around the world to spend one, six, or twelve weeks in New York focused on getting better at programming. <br/>2. The primary educational value of RC is peer-to peer. We don’t have teachers or a curriculum <br/>3. Recursers work on whatever they’re most interested in, teaching and learning from each other |
| [about page](https://www.recurse.com/about) | 2/2018 | 4. Batches start every six weeks . <br/> 5. We started RC in 2011, and for the first several years, we mistakenly organized our company into two divisions: education and recruiting <br/> 6. We charge 25% of first year salary from hiring company, nothing for the candidate |

### How to get users

## Building Website

### Tech Stack

## Components to Build
| Component | Notes | Notes 2 |
| -------   | ----- | ----    | 
| Env Setup | Take digital ocean one click install for Django .. |   |
| Django-allauth | take this documentation and try to implement  | [URL](http://django-allauth.readthedocs.io/en/latest/installation.html) |
| DB model | define Model in Django models.py file | take one of existing models .. |


see what Two scoops book saying about this Django-allauth

Write about what are the stacks considered & why


## Features
### 1. Live programming 
- It has both LPM and step back & step forward (when I tested)
- change top box to text as  "Write code in `Python 3`" , remove all top & bottom text
- let it work with above changes on Flask, then make it work on Django

### 2. User Registration & Login
- Provising & config of Django with Ansible (from the git repo). No Docker things at this time
- selection of User registration (China onlineJudge codebase, combine this with Django allauth for Social Login)

### 3. Voice Integration : TTS
- Amazon voice
- Sample audio read see how aduio feels [in a long page read](http://slideplayer.com/slide/10836541/)
 
 
 ## Version 2 features
 
 ### autocompletion
 - It may be good to add this RealTime web editor of python tutor
 - `Jedi ` library seems [best one]() , used by Atom, Sublime Text,  
 - Jedi can currently be used with the following editors/projects: 
 - some web specic (not desktop) implementaionts : [on Atom](https://atom.io/packages/autocomplete-python-jedi), working with [wdb](https://github.com/Kozea/wdb)
 
 ### web debugger
 - pythontutor only provides step thru, if advanced user wanted to tinker with `python interacitve shell` like we do one on PC/Mac installed python
  we can not do, but with this WDB we can same on the web
 - wdb : An improbable [web debugger through WebSockets](https://github.com/Kozea/wdb)
 - seems you can debug Flask, Django webserver code also ...