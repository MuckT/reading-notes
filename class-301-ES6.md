# 301 Prep ES6 reading notes

## ES6 Classes

### Objects and Inheritance

* JavaScript objects use [prototype-based inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain).

* JavaScript class and extends keywords internally JavaScript will still use prototype-based inheritance. It just simplifies the syntax (this is often called “Syntactic Sugar”).

* Similar but different to from [class inheritance](https://www.tutorialspoint.com/java/java_inheritance.htm) in strictly Object Oriented Programming languages like Java and C#.

### ES6 Classes

* Classes are standalone, self-contained object (instance) factories - Ultimately, they result in a prototype.

* `function()` becomes `class {}` & `call()` becomes `extends`

```JavaScript
// Using Prototypal Inheritance
function Animal(name) {
  this.name = name;
}
Animal.prototype.walk = function() {}

function Bird(name) {
  // I can do all the things animals can do!
  Animal.call(this, name);
}
// Unlike other animals, birds can fly
Bird.prototype.fly = function() {}

// Make a new bird ..
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();
```

```JavaScript
// Using ES6 Classes
class Animal {
  constructor(name) {
    this.name  = name;
  }
  walk() {}
}

// Thanks to 'extends', all birds can now do all things animals can
class Bird extends Animal {
  // Birds can walk, becuase they're animals also do their own thing.
  fly() {}
}

// Make one (the same was as before, but wasn't the class creation much easier?)
let parrot = new Bird('parrot');
parrot.fly();
parrot.walk();
```

### Additional Resources

[Sample with Prototypes & ES6 Classes](https://replit.com/@MuckT/ES6-Classes#vehicles-with-constructor.js)

[MDN inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

[MDN this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

[MDN class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
