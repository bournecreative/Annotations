# Page Loading

The life cycle of an HTML page has 3 important events.

**DOMContentLoaded event:** the browser fully loads the html, the DOM tree is built but external resources like image and style sheets may not be loaded yet

**onload event:** external resources like image and style sheets are loaded 

**beforeunload event:** right before user leaves page. we can check if user saved changes, ask if they really want to leave

**onunload:** user is just about left the page. Send out statistics

{% hint style="info" %}
Script tags will be parsed before the **DOMContentLoaded** is fired. There are only 2 exceptions for this rule.

Scripts with an _**async**_ attribute

Scripts that are generated dynamically with `document.createElement('script')` and are then added to the webpage.
{% endhint %}

### DOMContentLoaded

```
document.addEventListener("DOMContentLoaded", function(){
    do stuff....
}
```

### onload

```text
window.addEventListener('onload', function(){
    do stuff...
})

or 

window.onload = function (){
    do stuff...
}
```

### onbeforeunload

```text
window.addEventListener('onbeforeunload', function(){
    do stuff...
})

or 

window.onbeforeunload = function (){
    do stuff...
}

```

### onunload

```text
window.addEventListener('onunload', function(){
    do stuff...
})

or 

window.onunload = function (){
    do stuff...
}
```

### Testing the DOM state

At times, we may be unsure whether a document is ready or not. We can test the DOM state with `document.readyState`

```text
document.readyState // has 3 possible values

"loading" - indicates document is loading

"interactive" - indicates document was fully read

"complete" - indicates document was fully read and all resources are loaded.
```

The following is a general sequence of how we should expect the state of the DOM to load.

1. readyState: loading
2. readState: Interactive
3. DOMContentLoaded
4. onload
5. readyState:complete
6. window:onload



