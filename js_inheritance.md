# JAVASCRIPT INHERITANCE #


## [MDN: Inheritance and the prototype chain](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain) ##
* dynamic
* does not provide a class implementation
  * but class is a reserved keyword


#### Objects ####
* Javascript's construct
* "bags" of properties


#### Prototype ####
* object's internal link to another object
* has a prototype of its own
* ``null`` - final link in the prototype chain


#### Review creating an Object ####

* syntax constructs

```js
    var o = { a: 1 }; //inherits from Object.prototype, which inherits from null
    var a = [1, 'b']; //inherits from Array.prototype, which inherits from Object.prototype
    function f(){ return 'this is a function'; } //inherits from Function.prototype, which inherits from Object.prototype?
```


* constructor (``new operator``)

```js
function Person(name){
  this.name = name
}

Person.prototype.sayName = function(){
  return 'My name is ' + this.name;
}

var john = new Person('john'); //inherits from Person
```


* ``Object.create(prototype)`` (introduced by [ECMAScript 5](https://en.wikipedia.org/wiki/ECMAScript))
  * creates a new object

```js
  var Parent = {
    x: 1,
    y: function(){
      return this.x + 1;
    }
  }
  
  var child = Object.create(Parent); //inherits from Parent
  var subchild = Object.create(child); //inherits from child
```


#### Inheriting "methods" ####
* any function can be added to an object in the form of property
* inherited function acts just as any other properties

---


## Different Inheritance Approach ##

#### John Resig ####
    
* [Simple Javascript Inheritance](http://ejohn.org/blog/simple-javascript-inheritance)
  * http://jsfiddle.net/rE3xQ/2/


#### Douglas Crockford ####
* [Classical Inheritance in Javascript](http://www.crockford.com/javascript/inheritance.html)
  * http://jsfiddle.net/ykDdu/1/


#### Gavin Kistner ####
* [Convenient Inheritance](http://phrogz.net/js/classes/OOPinJS2.html)
  * http://jsfiddle.net/jjLQP/1/
