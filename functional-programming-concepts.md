# Functional Programming Concepts

## Immutable Data

What is simpler to maintain - data that changes or data that does not? 

How might we manage changes in state with the presupposition that we are working with immutable data? Lets first begin by looking into how we can work with immutable data.

### Managing data in an immutable way

#### Spread operator \| adding and updating object properties

The spread operator is new syntax that allows for a more terse means of coping objects.  The key take away illustrated below is that we are able to add to and update property names of our new object _ArcTrooper_ while not mutating the original details of the object _trooper_. 

```
const trooper = {
    trooperId: 117,
    type: "Storm Trooper",
    weapon: "blaster rifle",
    side-arm: "pistol",
    armor: 1
}

const snowTrooper = {
    ...trooper,
    trooperId: 32,
    type: "snow",
    weapon: "pulse canon",
    side-arm: "pistol",
    armor: 3
}
// make note of where the spread operator is in relation to the
// properties being added and updated
```

{% hint style="info" %}
JavaScript does not support immutable data all that well. Although the const key word prevents us from reassigning values to a constant, it does not prevent us from reassigning property values of an object.
{% endhint %}

#### Spread operator \| deleting object properties

The spread operator can also enable us to delete object properties in an immutable way

```text
const {weapon ...ATATdriver} = trooper
// make note of where the spread is in relation to the property
// being removed
```

Also make note that we also make use of _**destructuring.**_ What is _**destructuring**_ you ask? 

_**Destructuring**_ **is a means of unpacking properties of an object directly into variables.** 

```text
const applePie = {
    filling: "apples",
    topping: "sugar and spice"
}

// const filling = pie.filling
// const topping = pie.topping

// A faster way to do this
const {
    filling,
    topping
} = applePie

console.log(filling)
console.log(topping)
```

