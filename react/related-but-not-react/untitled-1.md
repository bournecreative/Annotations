# ES6 Modules

When using ES6 modules we need to remember that we need to always **import** our dependencies at the top of page and **export** our components at the end of the page

### Importing

To make use of installed components, we must reference them

```
import defaultExport from 'packageName'

//Example
import React from 'react';
```

{% hint style="info" %}
You must import all necessary dependencies at the top of the page.
{% endhint %}

### Only importing select methods from a Package

```text
import { methodName } from Component

import { render } from 'react-dom'
```

#### Importing multiple methods from a Package

```text
import { BrowserRouter, Switch, Route } from 'react-router-dom;
```

### Importing Components Created

{% hint style="info" %}
When we are importing files that we create, not libraries. We need to specify the _**file name**_ where we typically identify the _**variable name**_ and we need to identify the _**file path**_ rather then the library name.
{% endhint %}

```text
import ComponentName from Component Path Name

 import StoreLocator from './components/StoreLocator' 
```

### Importing functions from Stateless Components

```text
import methodName from Component Path Name

 import {filterURL} from './components/helpers' 
```

### Exporting

If you intend on using a component, you need to ensure you make that available to outside components. You do this by exporting.

```text
export default ComponentName

//Example
export default CarLocation
```

#### Named Exports

Importing select methods from a package requires that we also export those functions

```text
export function locateDevice (){
  ...
}
```

