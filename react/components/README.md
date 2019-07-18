# Components

## The concept of components

When we look at HTML tags, we can each see that each type of tag is defined with specific purpose, with unique functionality and characteristics. React components reflect this concept, but allow you to create and define how they function and integrate with other components. 

{% hint style="success" %}
The beauty of React is its ability to manage state throughout the components. 
{% endhint %}

### Creating a react component

```text
import React from 'react'
import ReactDOM from 'react-dom'

// capitalize class name
// components need a render method

class StorePicker extends React.component {
    render(){
        return <p>Hello There </p>
    }
}

default export StorePicker
```

{% hint style="info" %}
The render method determines what HTML is rendered from the component. Render methods return JSX which looks like html but is really JavaScript
{% endhint %}

{% hint style="info" %}
The is the mounting point
{% endhint %}

### Importing react-dom

Rather then import the entire react-dom library, we only import a single function needed from react-dom

```text
// Importing the render function
import {render} from 'react-dom'
```

{% hint style="info" %}
The render method takes 2 arguments

1. JSX to render. We pass the parent class of our React application
2. Mounting point. The mounting points is the DOM element your application hooks into
{% endhint %}

```text
render(parentClass, mounting point)

render(<StorePicker />, document.querySelector('#main'))
```

