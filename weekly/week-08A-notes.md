# Week 8A - More ES6 Classes and Modules / Midterm Questions

## I. Overview
- The midterm exam is next time - any questions?
- The Project 2 requirements are posted here: [Project 2 - HTML5 Canvas Experience or Game](../projects/project-2.md) - and there is a discussion thread in mycourses where you will need to post whether you are working solo or with a partner
- We will continue our discussion of JS objects and modules - [About this Canvas Sprites Tutorial Series](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-0.md)


## II. Lecture Notes
- [1 - Intro to Canvas Sprites](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-1.md)
  - First we try to build a sprite object using script-scoped variables such as `x`, `y`, `radius`, `color`  - BAD!
  - then we group these variables into an object literal - BETTER!
  - lastly we create a factory function to produce multiple object literals - BEST!
  - take a look in the web inspector to see these objects and the default *prototype chains* created via the `__prototype__` - i.e. "dunder proto" property - http://2ality.com/2012/10/dunder.html - we will discuss  *prototype* chains soon
  - isn't this inefficient, storing multiple copies of all of these properties and methods?
    - In a class-based environment, each instance of a class would have their own copies of instance variables (like `x` and `y`), but share all of the methods (like `move()`, `reflectX()`, and `reflectY()`)
    - interestingly, all major JavaScript engines already perform this optimization on object literals, and basically generate a "super class/super object" for you. The concept is called *shapes*, and you can read about it here: https://mathiasbynens.be/notes/shapes-ics
    -  No matter how many objects there are, as long as they have the same *shape*, they only have to store the shape and property information once. All JavaScript engines use shapes as an optimization, but they don't all call them shapes:
        - Academic papers call them *Hidden Classes* (confusing w.r.t. JavaScript classes)
        - [V8](https://github.com/v8/v8) calls them *Maps* (confusing w.r.t. JavaScript Maps)
        - [Chakra](https://github.com/Microsoft/ChakraCore) calls them *Types* (confusing w.r.t. JavaScript’s dynamic types and typeof)
        - [JavaScriptCore](https://trac.webkit.org/wiki/JavaScriptCore) calls them *Structures*
        - [SpiderMonkey](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/SpiderMonkey) calls them *Shapes*
        
- [2 - Object.create() & Delegation](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-2.md)
  - In JavaScript, how can we benefit from the concept of `inheritance` without using classes - answer: the JavaScript *prototype chain*:
    - this is called *prototype-based inheritance*
    - "own" properties and properties 
    - *property shadowing* is basically like "overriding" in class-based languages
  - `Object.create()`
  - Delegation & OLOO - "Objects Linked to Other Objects"
  
- [3 - Canvas & ES6 Classes](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-3.md)
  - JavaScript classes = "syntactical sugar"!
    - but sugar tastes so good!
    - even with classes, behind the scenes, the JS engine is still using the *prototype chain*
    - POLL: do you prefer ES5 delegation, or ES6 classes?
    

## III. Required Reading & Assignments
- [4 - JavaScript & ES6 Modules](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-4.md)
- [5 - JavaScript & the ES5 Revealing Module Pattern](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-5.md)
- [6 - Transpiling ES6 to ES5](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-sprites-6.md)



<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-07-notes.md**](week-07-notes.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**week-08B-notes.md**](week-08B-notes.md)
