
## Kitchen Sink Code

- [Typewriter lib](https://safi.me.uk/typewriterjs/) working on a "DIV" on [Jsfille](https://jsfiddle.net/mv612vrf/1702/?utm_source=website&utm_medium=embed&utm_campaign=mv612vrf)
- Ace Editor [JSFiddle simple one](http://jsfiddle.net/Yzj6G/)

- Add the following code to above Ace Editor JS Fiddle in the 'JS code window' , TypeWriter effect (with delays etc.. ) start working on the Ace Editor filed .
```
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
