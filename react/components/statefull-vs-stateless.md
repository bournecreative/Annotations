# State-full vs Stateless

### Stateless Components

Components that only render content and do not manage state can be converted into a stateless functional components. _**Stateless functional components**_ are not considered React class objects

```text
function Header(){
    return (
        <header>
            <h3 className="tagLine">Static Text</h3>
        </headr
    }
}
```

{% hint style="info" %}
You can pass data to stateless components. However, "this" does not exist for these components. Stateless functional components take one argument _**props**_
{% endhint %}

```text
function Header(props){
    return (
        <header>
            <h3 className="tagLine">{props.tagline}</h3>
        </headr
    }
}
```

### State-full Components



