# Page Loading

The life cycle of an HTML page has 3 important events.

**DOMContentLoaded event:** the browser fully loads the html, the DOM tree is built but external resources like image and style sheets may not be loaded yet

**onload event:** external resources like image and style sheets are loaded 

**beforeunload event:** user leaves page

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

### onunload

```text
window.addEventListener('onunload', function(){
    do stuff...
})

or 

window.onbeforeunload = function (){
    do stuff...
}
```

### onbeforeunload

```text
window.addEventListener('onbeforeunload', function(){
    do stuff...
})

```



