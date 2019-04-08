# Functional Programming Concepts

## Immutable Data

What is simpler to maintain - data that changes or data that does not? 

How might we manage changes in state with the presupposition that we are working with immutable data?

{% hint style="info" %}
JavaScript does not support immutable data all that well. Although the const key word prevents us from reassigning values to a constant, it does not prevent us from reassigning property values of an object.
{% endhint %}

### Spread operator

The spread operator is new syntax that allows for a more terse means of coping objects.  The key take away illustrated is that we are able to add to and update properties names of the original object _trooper_ while not mutating the original state of the _trooper_ object. 

```
const trooper = {
    base: "Storm Trooper",
    weapon: "blaster rifle",
    armor: 1
}

const ArcTrooper = {
    ...trooper,
    class: "Arc Trooper"
    weapon: "pulse canon"
} 
```

