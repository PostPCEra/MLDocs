---
id: 33_Product_featuers
title: Product featuers & PRD
sidebar_label: Product featuers & PRD
---


## Features

**move PRD & Docusarus to Bitbucket** , start using Digital ocean 2 month credit with Django/Ansible ..

### 1. Live programming 
- It has both LPM and step back & step forward (when I tested)
- change top box to text as  "Write code in `Python 3`" , remove all top & bottom text
- let it work with above changes on Flask, then make it work on Django

### 2. User Registration & Login
- 10/1: just have a input Text box to choose a unique ID and click submit, then onwards <UniqueID> is appened to URL
  and file saving etc.. is handled with hat <UniqueID>
- Provising & config of Django with Ansible (from the git repo). No Docker things at this time
- selection of User registration (China onlineJudge codebase, combine this with Django allauth for Social Login)

### 3. Pedagogy
- daily effort 1 hr min ( preferably in one sitting) 
- finish TEST at the end of session EVERY DAY ( should be strictly followed)
- weekend Tests
- peer grading
- write in your own words what a FOR , IF means ; write a real world analogy ( version it & let them see 1 month old def of FOR , IF). 
- 9/15/18 :see this FOR loop blanks example https://twitter.com/PostPCEra/status/1034166441782665219
- on paper tests

- 10/1/18: A CEFR-like approach to measure programming proficiency https://science.raphael.poss.name/programming-levels.html tweet https://twitter.com/PostPCEra/status/1046880352428380160 ( see pic on tweet showing 'cumulative hours' for given Level)
```
3 broad levles:
Writing
Understanding
Interacting

(A1, A2, B1, B2, C1, C2) : testable milestones in language acquisition

For our ML Python Course learing:
  - we comeup with similar A1 .. C2 6 six levels
  - for Column headings : we wil have ( see more from programirz etc.. )
  - we will have this chart as 'Front & Center' of the Teaching, any time student can popup. Student has pass TESTS of
    a given Level 'A1 of Funcitons' before allowed to move to 'A2 of Functions' etc. We show hours spent on a level
       -------------- |--------------------| -------------- | ----------- | ---------- | ----------- | ----------- |
                          A1 Level         | A2             | B1          | B2 Level   | C1          |   C2        |     
       -------------- |------------------- | -------------- | ----------- | ---------- | ----------- | ----------- |                 
     Basics           | variables,data types| 
     Control Flow     | IF ..Else, Loops  |nested loops    | combination loops
     Functions        | parameters        | Recursion      |  
     FLow Chart       | simple one        |
     Data structures  | List              | Dictionalry    |  
     File handling    | File Operations   | Exception      |              |               |  
     Object & Class   | Python OOP        | Class          | Inheritance  | Multiple Inheritance |  
```
[programiz](https://www.programiz.com/python-programming#tutorial) <-- refer to this to get more details 


### 3.2 Exercises & Tests
- we need this asap. Khan academy have a frame work to create Tests? see others 


### 4. Forum software : Discourse
-  go with $20/month plan?, should we ask to try this with 2 month Trail? .. 

### 5. Start talking to users
-  Art of living , later Empower & Excell , and Summer fre Tution fixed time classes 

### 6. Voice Integration : TTS
- 9/15/18: Google Text to Speech TTS
-  Google Deep mind [AI drive Wavenet TTS better quality](https://www.theverge.com/2018/3/27/17167200/google-ai-speech-tts-cloud-deepmind-wavenet)
- Listen to voices, u can very [Speed & Pitch combinatons](https://cloud.google.com/text-to-speech/)
- Price: 1 Million chars free/month, [next Mil $16](https://cloud.google.com/text-to-speech/pricing) , -- [python API](https://github.com/GoogleCloudPlatform/python-docs-samples/tree/master/texttospeech/cloud-client)
----
- Amazon voice
- Sample audio read see how aduio feels [in a long page read](http://slideplayer.com/slide/10836541/)
 
### 7. animation 
- 9/29 : Animatron web site looks [simple to make Lesson videos](https://www.animatron.com/)
- see old research on animation 
 
 ## Version 2 features
 
 ### 1. autocompletion
 - It may be good to add this RealTime web editor of python tutor
 - `Jedi ` library seems [best one]() , used by Atom, Sublime Text,  
 - Jedi can currently be used with the following editors/projects: 
 - some web specic (not desktop) implementaionts : [on Atom](https://atom.io/packages/autocomplete-python-jedi), working with [wdb](https://github.com/Kozea/wdb)
 
 ### 2. web debugger
 - pythontutor only provides step thru, if advanced user wanted to tinker with `python interacitve shell` like we do one on PC/Mac installed python
  we can not do, but with this WDB we can same on the web
 - wdb : An improbable [web debugger through WebSockets](https://github.com/Kozea/wdb)
 - seems you can debug Flask, Django webserver code also ...
