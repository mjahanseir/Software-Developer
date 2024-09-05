02- Prototypes and Prototypical Inheritance

To implement inheritance in JavaScript objects following the example:

![Prototypical Inheritance](./images/02-01.png "Prototypical Inheritance")

We implemente the common methods in the Shape object. We refer to the Shape object as the Prototype of the Circle. Prototype is essencial the parent of another object

Every object in JavaScript has a parent object, when we create a object, if we inspect that object in tha console we can see the following:

```javascript
let x = {};
// __proto__:
//     constructor: ƒ Object()
//     hasOwnProperty: ƒ hasOwnProperty()
//     isPrototypeOf: ƒ isPrototypeOf()
//     propertyIsEnumerable: ƒ propertyIsEnumerable()
//     toLocaleString: ƒ toLocaleString()
//     toString: ƒ toString()
//     valueOf: ƒ valueOf()
//     __defineGetter__: ƒ __defineGetter__()
//     __defineSetter__: ƒ __defineSetter__()
//     __lookupGetter__: ƒ __lookupGetter__()
//     __lookupSetter__: ƒ __lookupSetter__()
//     get __proto__: ƒ __proto__()
//     set __proto__: ƒ __proto__()
```

The property called `__proto__` is deprecated.

We can call any of this methods in our x object.

So x in an object and it has a link to another object, which is it's Prototype. This prototype, let's call it `objectBase`. Every Object in JavaScript inherits directly or indirectly from `objectBase`.

`objectBase` is the root of all object in JavaScript, and it does not have a parent or Prototype.

To get the Prototype of an object we can use: `Object.getPrototypeOf(x);`

When we call a method in an object JavaScript will start looking for that method in the object it self. If we can't find it will go all the way up to the root object we called objectBase.

A prototype is just a regular object in memory.
