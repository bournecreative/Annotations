# State

State is initialized at the top of our application and becomes available to lower level components.

Initial State can be set in the constructor of the parent component

```text
constructor(){
    super();
    this.state = ""
}
```

State can also be initialized as an object like so

```text
state = {
    tshirts: {},
    order: {}  
}
```

### Updating State

{% hint style="info" %}
Note that the initialized state and the methods to update that state need to live or originate in that original component.
{% endhint %}

{% hint style="warning" %}
When updating state we always take a copy of state and update. No mutations
{% endhint %}

```text
addShirt(shirt){
    
    //take a copy of state
    const shirts = {...this.state.tshirts}
    
    //add new shirt to shirts var
    shirts[`shirt${Date.now()}`]
    
    //set state of tshirts to value of var shirts
    this.setState({
        tshirts: shirts
    })
}
```

