# ES6 Modules

### Importing

To make use of packages installed, we must reference them in our source javascript

```
import VariableName from 'packageName'

//Example
import React from 'react';
```

{% hint style="info" %}
You must import all necessary dependencies at the top of the page.
{% endhint %}

### Importing only what you need

Rather then import entire libraries, we can choose to import single functions.

```text
import {functionName} from 'packageName'

// Importing the render function from react-dom

import {render} from 'react-dom'
```

{% hint style="info" %}
When we are importing files that we create, not libraries. We need to specify the fileName where we typically identify the variable name and we need to identify the file path rather then the library name
{% endhint %}

```text
import Component Name from 'relative path to Component'

// Example
import CarLocation from './components/CarLocation'
```

### Exporting

If you intend on using a component, you need to ensure you make that available to outside components. You do this by exporting.

```text
export default ComponentName

//Example
export default CarLocation
```

