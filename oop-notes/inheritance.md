# Inheritance

## The corner stone of re-usability

Inheritance is one of the core concepts of oop that enable children objects to take on the properties and methods of parent objects. Because of inheritance, code can be reused as demonstrated in the following examples.

### Classical inheritance

Rather than have objects with identical properties and methods, we can have children objects inherit methods and properties from a parent object. This example illustrates inheritance via object classes.

![](../.gitbook/assets/screen-shot-2019-07-16-at-2.38.36-pm.png)

### Prototypical inheritance

{% hint style="info" %}
In JavaScript we do not have classes, we only have objects. However the same principal of inheritance can work because of the _**prototype.**_

Every object in JavaScript has a prototype except the _**root object. The prototype can be thought of as a parent object from which the current level object inherits from.**_
{% endhint %}

### Who is my Parent?

We can identity what the prototype of an object is with the following method:

```text
Object.getPrototypeOf(obj) // returns the prototype object
```

We can also determine the prototype by inspecting an object in dev tools.

{% hint style="info" %}
look for the \_\_proto\_\_ property
{% endhint %}

![myArray inherits from arrayBase and arrayBase inherits from objectBase](../.gitbook/assets/screen-shot-2019-07-16-at-2.49.08-pm.png)

{% hint style="info" %}
If we were to inspect each of these objects, we would notice a property called _**\_\_proto\_\_**_ which would list the inherited properties and methods. Although _**\_\_proto\_\_**_ is the property the inspector displays, DO NOT use _**\_\_proto\_\_**_ as it is deprecated property
{% endhint %}

### The big picture

When we use a constructor from which we can use to create object instances from, know that each instance of that object is inheriting the properties and methods from that constructor instance.

Also understand that the constructor is also inheriting properties and methods from its prototype. This prototype can be accessed via:

```text
// Obj.prototype is the property used to represent the parent object
// used to create the current level object. 
Obj.prototype 
```

Because JavaScript is dynamic we can always add to objects.

{% hint style="warning" %}
Being able to add properties and methods to the prototype object is powerful but "With great power comes great responsibility".
{% endhint %}

```text
Object.prototype.methodtoAdd = function(){
    ...do stuff
}
```

So this is kind of crazy, we technically have 2 types of properties methods that can be accessed from the object.

1. Properties and methods defined within an instance of an object - **instance members**
2. Properties and methods defined within an objects prototype object - **prototype members**

{% hint style="success" %}
Prototype methods and properties work just like their instance counter parts. However there is a benefit to adding methods to the prototype object. Functions are saved in memory. If there are numerous instances of such an object, there are a lot of copies of the same functions all held in memory. If the functions are however inheritied from the prototype, then only 1 copy of the function is held in memory regardless of the number of objects instances in play.
{% endhint %}

