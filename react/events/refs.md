# Refs

_**Ref**_ is short for _**References**_

In React, we avoid referencing the DOM using our standard methods of selecting DOM elements with vanilla JavaScript or jQuery. With _**Refs**_, it is possible to _reference_ the values of the DOM rather then leveraging State.

```text
class Messenger extends React.Component {
    constructor(){
        super()
        this.eventHandlerExample = this.eventHandlerExample.bind(this)
    }
    
    myMessage = React.createRef();
    
    eventHandlerExample(e){
        //we can access the reference of the input value here
        console.log(this.myMessage.value.value)
    }
    
    render() {
        return (
            <input 
                type="text"
                ref={this.myMessage}
            />
            ... more JSX
        )
    }
}    
```

{% hint style="info" %}
Creating a _**ref**_ will enable that value to be referenced within that class component
{% endhint %}

