

## Task list 
```
- 1. Google TTS integration
- 2. Bitbucket git setup : do only v5-unity dir
- 3. Make Lesson content
   
 - 4. Site up & running on Digital Ocean
 - 5. Discourse Forum software
 - 6. 

```
#### 3. Make Lesson content
```
 1. see Programirz & other sites for content
     - what is programming : series of steps , rectangle 5 th grade math problem (area = length * width)
     - show a english paragraph. one with lots of spaces between words, words broken in lines , good one . A programmer's wife.
     - ask to wrong assignments or statements 
 2. only WHILE loop ( FOR never). what is it, list of fruits , show list of names . first item in fruit list : apple ,  fruits[1] .. fruits[3]
     apple
     oragne
     banana
     
 3. Block of code : show two sections (/w IF else..) of same english text one with {  } , the other with identation , python chose 2nd one
     
```

#### 8. Helping others ( colloboration )
```
 - Teacher/Leaner model 
 - use Pturor collob feature,  have   'stage 1',  'state 2' , buttons let Teacher save them at diff points in time
 - so Learner can  replay to see how  the code correciton progressed. Learner can add comment text as he understand 
 - Learner need to write a small write up of problem so Teacher can look and understand before helping .
```


## Kitchen Sink Code

#### 1. Ace Editor & Typewriter lib integration 

- [Typewriter lib](https://safi.me.uk/typewriterjs/) working on a "DIV" on [Jsfille](https://jsfiddle.net/mv612vrf/1702/?utm_source=website&utm_medium=embed&utm_campaign=mv612vrf)
- Ace Editor [JSFiddle simple one](http://jsfiddle.net/Yzj6G/)

- Add the following code (of above Typewriter Fidle) to above Ace Editor JS Fiddle in the 'JS code window' , TypeWriter effect (with delays etc.. ) start working on the Ace Editor filed .
- This whole working thing is saved as my own fiddle at http://jsfiddle.net/vision/we3qs98k/
```
Add this url to the Library list in the Left menu.
// https://unpkg.com/typewriter-effect@2.3.1/dist/core.js

var app = document.getElementById('editor');

var typewriter = new Typewriter(app, {
    loop: true
});

typewriter.typeString('Hello World!')
    .pauseFor(2500)
    .deleteAll()
    .typeString('Strings can be removed')
    .pauseFor(2500)
    .deleteChars(7)
    .typeString('<strong>altered!</strong>')
    .pauseFor(2500)
    .start();
```
