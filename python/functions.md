# Functions

Functions are reusable blocks of code that take in input, process those arguments and return an output.

### Built-in Functions

```
myVar = type(5)
// returns integer

print(myVar)
// prints myVar

int(5.5)
// Parses floats into integers

sorted("file1", "file2")
// sorted alphabetically

sum([1,2,3])
// sums tuple

min([5,3,7])
// outputs min

max([5,3,7])
// outputs max
```

{% embed url="https://docs.python.org/3/library/functions.html" %}

### Importing Functions you don't have

```text
import <package name>

import datetime

// you can then access the package methods through its container object
myDateTime = datatime.strptime(...)

// importing specific methods

from datetime import datetime

// now we dont need to reference the datetime object name when calling methods

// Importing all methods from a package. This is not advised because it is unlikely you
// need the entire library

import datetime import * 

```

### Creating your own functions

Say we wanted to encapsulation the following into a function

```text
myStr = 'California'

if len(myStr) % 2 == 0:
    print('Even')
else:
    print('Odd')
```

#### Define function

```text
// functions do not require arguments, but can also have mulitple arguments
// all code within code block must be indented
// you do not need to have a return statement
// you can return more then 1 value
// variables are scoped just like javaScript

def evenOdd(string):
    if len(string) % 2 == 0:
        evenOdd = 'Even'
    else:
        evenOdd = 'Odd'
    returns evenOdd
```

#### Once the function is defined, you can invoke it just like any other function

```text
evenOdd('jedi')
```

### Other notes about Functions

Functions Scope works similar to JavaScript

Also like JavaScript, when you define a function with arguments. You must invoke the function using arguments in the same order at which they were defined in the function

You can define argument values when invoking a function

```text
def myFunction(arg1, arg2, arg3){
    ...code block
}

myfunction(arg1=100, arg3="plus", arg2=2)
// because we have specified the arg position with value, the function does not need to
// invoke the function with its arguments in defined order
```



