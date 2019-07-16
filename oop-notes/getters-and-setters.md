# Getters & Setters

## Some Context

```text
function deviceObj(){

    // we create a variable to represent a value
    let deviceID = model.deviceID;
    
    // to get this value, we create a method to return the value
    this.getDeviceID = function(){
        return deviceID;
    }
} 
```

### There has to be a better way?

Say we wanted to retrieve the deviceID as a property rather then a method - `deviceObj.deviceID`

{% hint style="info" %}
Objects come with a predefined method called **defineProperty.** 

**defineProperty** takes 3 arguments:

* the object we want to add a new property to. In this case we are defining a property to the object we are working within so we will use the keyword '**this'**
* the name of the property we want to define - **deviceID**
* a key value pair:
  * get and a method
  * OR
  * set and a method
{% endhint %}

#### Getter

This is known as creating a computed property. Getter are read only.

```text
Object.defineProperty(this, deviceID, {
    get: function(){
        return deviceID
    }
})
```

{% hint style="warning" %}
When we type deviceObj.deviceID the getter we defined will deliver the value of the deviceID variable as if it were a property of deviceObj
{% endhint %}

#### Setter

Another form of a computed property. Setters can set as the name implies and we can even include logic to ensure values are set properly.

```text
Object.defineProperty(this, 'zipCode', {
    set: function(value){
        if (...!some regex)
            throw new Error('Invalid zip code')
        
        zipCode = value;
    }
})
```

