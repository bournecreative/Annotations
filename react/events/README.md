# Events

## Events are just like JavaScript Events with a few exceptions

### All React events are wrapped in a Synthetic Wrapper

1. Because of this, event Handlers have slightly different naming conventions
2. Events are written inline within JSX

```text
handleClick(){
    ...handler logic
}

render(){
    return (
        ... stuff
        <button onClick={this.handleClick}>Click here</button>
    )
}
```

#### If you want an event handler to run when the component mounts

```text
 // invoke the click handler
 <button onClick={this.handleClick()}>Click here</button>
```

{% hint style="info" %}
event.preventDefault\(\) works as expected
{% endhint %}



