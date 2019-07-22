# Routing

Routing is actually a separate Component  

### Importing Methods For React Router

```text
import { BrowserRouter, Route, Switch } from 'react-router-dom'
```

### SetUp

```text
function Router(){
    return (
        <BrowserRouter>
            <Switch>
                <Route></Route>
                <Route></Route>
                <Route></Route>
            </Switch>
        </BrowserRouter>
    )
}
```

### Arguments of Router

Based on the arguments passed to React Router, its behavior changes.

```text
<Route exact path="/" component={}>
```

**`exact`** indicates that path must the defined path exactly

**`path`** indicates the path

**`component`** indicates compute to push to. Remember to import components

{% hint style="info" %}
The routes set up inside the Switch component function just like a condition switch statement.

The final route is like a catch-all-clause which is why is does not have a path defined 
{% endhint %}

