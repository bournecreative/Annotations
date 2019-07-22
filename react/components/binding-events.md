# Binding Events

### Synthetic Event

Events work just as they do in React as they do with vanilla JavaScript except that they are wrapped in a Synthetic Event. This Synthetic Event wrapper ensures all events behave the same across all browsers.

#### Syntax

Event Listeners are added inline to the JSX within our components

```text
<button onClick={this.incrementCount}>Add</button>
```

### Refs

Refs allow us to reference elements like we normally do with `document.querySelector`

```text
varName = React.createRef();
```

### Preventing Default Events

```text
// function invoked by button submit
getInfo(event){
    event.preventDefault();
    ... function logic
}
```

### Working with This and Class Components

When working within class components, if you reference `this` within the component's render function, `this` refers to the component.

Within the same component, if you reference `this` above the render function you will get _**undefined.**_ Why?

#### Because of Binding

 When we create a class component, we _**extend React.Component**_

```text
class droneTorpedo extends React.Component {
```

This means that all React component functions like `render()` or `componentDidMount`  already reference the correct pointers because they are all children methods of React.Component.  

But any methods or events we build on top of this Component as we extend the class do not yet point to their correct reference. 

Option 1

```text
class droneTorpedo extends React.Component {
constructor(){
    super()
    this.igniteRocket = this.igniteRocket.bind(this)
}

```

Option 2

```text
igniteRocket = event => {
    event.preventDefault();
    ...function logic
}
```

