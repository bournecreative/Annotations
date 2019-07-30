# Getting to know React Hooks

## React Hooks

A Hook is a special function that lets you "hook" into React features. Hooks replace but do not eliminate class components. There are a variety of hooks that serve specific purposes. 

### Primary Hooks

State management

`useState()`

Introduce side-effects into code

`useEffect()`

Leverage context in new functional components

`useContext()`

### More Hooks

`useRef()`

`useReducer()`

### Quick example of the magic 

```text
import React, { useState } from 'react;

function Counter(){
const [count, setCount] = useState(0)

return (
    <div>
        <p>You clicked {count} times </p>
        <button onClick={() => setCount(count + 1)}
    </div>
    )
}
```

### Rules of Hooks

You call Hooks at the top level - not within loops, conditions or nested functions

You call Hooks only from React function components

### useState\(\)

We no longer need to use class components to leverage state.

1. Declare State

```text
const [count, setCount] = useState(0)

// useState returns a pair of values, the current state and a function that updates it
```

2. Updating State

```text
<button onClick={() => this.setCount(count + 1)}>Add One </button>
```

3. Reading State

```text
<p> You clicked {count} times!!</p>
// you simply reference the value used to represent the state value
```

