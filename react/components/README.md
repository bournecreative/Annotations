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
// ever component needs a render method 
class StorePicker extends React.component {
    render(){
        return <p>Hello There </p>
    }
}

default export StorePicker
```

The render method

{% hint style="info" %}
The render method determines what HTML is rendered from the component. Render methods return JSX
{% endhint %}

{% hint style="info" %}
The render method determines what HTML is rendered from the component. Render methods return JSX
{% endhint %}

{% hint style="info" %}

{% endhint %}

{% hint style="info" %}
JSX looks a lot like HTML but it is a terse syntax that is translated into vanilla javascript when compiled
{% endhint %}

### 2 Types of Componets

1. Stateless Components
2. Components with State



