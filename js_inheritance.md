# JAVASCRIPT INHERITANCE #


## MDN: Inheritance and the prototype chain ##
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


### Review creating and Object ###
1. syntax constructs

```js
  var o = { a: 1 }; //inherits from Object.prototype, which inherits from null
  var a = [1, 'b']; //inherits from Array.prototype, which inherits from Object.prototype
  function f(){ return 'this is a function'; } //inherits from Function.prototype, which inherits from Object.prototype?
```

2. constructor (``new operator``)

```js
function Person(name){
  this.name = name
}

Person.prototype.sayName = function(){
  return 'My name is ' + this.name;
}

var john = new Person('john'); //inherits from Person
```

3. ``Object.create(prototype)`` (introduced by ECMAScript 5)
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

### Inheriting "methods" ###
* any function can be added to an object in the form of property
* inherited function acts just as any other properties

---






http://jsfiddle.net/U2xTs/3/

http://jsfiddle.net/U2xTs/4/ << with super call

http://jsfiddle.net/rE3xQ/ << John Resig Approach

http://jsfiddle.net/ykDdu/ << Crockford Approach

http://jsfiddle.net/jjLQP/ << Gavin Kistner Approach


http://www.crockford.com/javascript/inheritance.html
http://ejohn.org/blog/simple-javascript-inheritance
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain
http://phrogz.net/js/classes/OOPinJS2.html
