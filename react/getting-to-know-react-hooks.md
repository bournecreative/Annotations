# Getting to know React Hooks

## Introducing some React Hooks

### Primary Hooks

State management

`UseState()`

Introduce side-effects into code

`UseEffect()`

Leverage context in new functional components

`UseContext()`

### More Hooks

`useRef()`

`useReducer()`

### Example 

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

