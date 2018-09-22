
## Kitchen Sink Code

#### 1. Ace Editor & Typewriter lib integration 

- [Typewriter lib](https://safi.me.uk/typewriterjs/) working on a "DIV" on [Jsfille](https://jsfiddle.net/mv612vrf/1702/?utm_source=website&utm_medium=embed&utm_campaign=mv612vrf)
- Ace Editor [JSFiddle simple one](http://jsfiddle.net/Yzj6G/)

- Add the following code (of above Typewriter Fidle) to above Ace Editor JS Fiddle in the 'JS code window' , TypeWriter effect (with delays etc.. ) start working on the Ace Editor filed .
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
