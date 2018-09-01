### Organising Personal Knowledge (notes)

##### Tools 
- Inspiration from Gordon: http://gordonbrander.com/pattern/
- Static site generators : [two popular ones](https://www.fullstackpython.com/static-site-generator.html) a) Pelican based: [fullstack python site](https://github.com/mattmakai/fullstackpython.com). b) Mkdocs  based: example [Django REST site](http://www.django-rest-framework.org/#api-guide). In MkDocs based seems good for Programmig guides like above Django REST API, where one full page LEFT menu links are same page with # anchors.  
- We go with Pelican, so is [recommended by this review](http://maxpearl.us/review-of-python-open-source-static-site-generators.html). Gordon used his own satic site generator, it is on his github repos. For us Pelican should do it

##### Format
- Have TOPIC content stored in YAML or similar format file, and let plug-in read and transform the content
- for UI page: Have Anchor links on top of page
```
   Learing , Feynmen (get from Gordon) , How Learning Works
   
   Abstracition , Library/Framework , 
```
- for a concept like 'Intelligence is capacity for Learning' when hover (or click) show popup with full content , that way easy navigation, not loosig context of current page. Use JS Lib for easy popup ..

- show images small as 100x100 px, when clicked show big popup image
- echo of these will have their own page: 
```
  Bookself 
  Stars, Evolution, World history 
  Autonomus vehicles, Renewable Energy : use BNEF tweets of total EV cars, EV buses stats, Solar/wind stats
```
- Have a Twitter dump into files with download , and use my best/popular tweets text, images and links
- for a page like 'Autonous vehicles', we can have page like this will 'References' at the bottom http://gordonbrander.com/pattern/conversational-ui/
