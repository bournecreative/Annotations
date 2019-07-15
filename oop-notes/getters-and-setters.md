# Getters & Setters

## Some Context

```text
function deviceObj(){
    let deviceID = model.deviceID;
    
    this.getDeviceID = function(){
        return deviceID;
    }
} 
```

But say we wanted to retrieve the deviceID as a property rather then a method - `deviceObj.deviceID`

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

```text
Object.defineProperty(this, deviceID, {
    get: function(){
        return deviceID
    }
})
```

{% hint style="warning" %}
When we type deviceObj.deviceID the getter we defined will deliever the value of the deviceID variable as if it were a property of deviceObj
{% endhint %}

