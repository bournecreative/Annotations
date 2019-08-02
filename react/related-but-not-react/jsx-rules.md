# JSX Rules

{% hint style="danger" %}
Whenever you are using JSX, remember to import React
{% endhint %}

When using JSX, there are a few rules to remember.

```
//example component

class tooltip extends React.Component{
    render(){
    return <tooltip></tooltip>
    }
}
```

{% hint style="info" %}
JSX must be returned on the same line as return because JSX uses ASI \(automatic semicolon insertion\)
{% endhint %}

```
//example component

class tooltip extends React.Component{
    render(){
        return (
            <tooltip></tooltip>
        )
    }
}
```

{% hint style="info" %}
You can wrap returned JSX in parentheses to format code in this indented variation to get around the issue noted previously with automatic semicolon insertion
{% endhint %}

```
//example component WRONG!!

class tooltip extends React.Component{
    render(){
        return (
            <tooltipContainer></tooltipContainer>
            <tooltip></tooltip>
        )
    }
}
```

{% hint style="danger" %}
You cannot insert multiple adjacent JSX tags as illustrated. They must be nested 
{% endhint %}

```
//example component GOOD

class tooltip extends React.Component{
    render(){
        return (
            <tooltipContainer>
                <tooltip></tooltip>
            </tooltipContainer>
        )
    }
}
```

As of **React 16.2**, there is an alternative solution if adjacent elements are required

```
//example component BETTER

class tooltip extends React.Component{
    render(){
        return (
            <React.Fragment>
                <heroText></heroText>
                <tooltipContainer>
                    <tooltip></tooltip>
                </tooltipContainer>
            <React.Fragment>
        )
    }
}
```

We can use `<Fragment>` rather then _`<React.Fragment>`_  

_**If and Only If**_ you import the _**React.Fragment**_ method from **react**

`import React, { Fragment } from 'react'`

