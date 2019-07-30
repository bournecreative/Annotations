# Props

Working with class components, props enable you to pass data as values to elements.  State can be thought of as the home for data and props is the vehicle to transport that data. 

{% hint style="info" %}
Props are passed from parent to children - top level down.
{% endhint %}

### We can think of props as data attributes

```text
<Headline titleText="Great deals today" dealPromotion={50} />
```

Once this data is made available from the parent components, the props may be referenced within the returned JSX

```text
class Headline extends React.Component {
    render();
        return (
            <header className="top">
                <h2>{this.props.titleText}! Priced Reduced by {this.props.dealPromotion}%</h2>
            </header>
        )   
}
```

{% hint style="info" %}
this is referring to the component instance
{% endhint %}

A really important take away from the note above, is that you can have multiple instances of components. When `this.props` is called, `this` is referring to the instance of that component. So you can have several instances of components and never have to worry about props not referencing the incorrect props values!



