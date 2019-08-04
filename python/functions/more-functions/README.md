# More Functions

## Map

Just like map with JavaScript with the exception of syntax. Takes an iterateable list and cycles through each item, just like a for loop but with in a different manner.

### Examples of Map

```text
def square(x):
    return x*2

myList = [1,4,6,8]

// map takes 2 arguments, the function to run against each list item and the list
// map returns a map object, you only get the object. You need to convert to a list 
// to see the values of the object
myObj = map(square, myList)
print(myObj) //obj that is returned
newList = list(myObj)
print(newList)
```

```text
myList = ['234234,'2342','23424']

numList - map(int, myList)
for item in numList:
    print(item)
```

```text
myList = [10,20,30,40]

listObj = map(lambda x: x - 10, myList)
for item in listObj:
    print(item)
    
```

#### Lambda Functions

Lambda let you create inline anonymous functions

```text
// as seen above 
// lambda keyword indicates you are going to write an inline function
// function must be 1 line
// lambda takes x and then does whatever you are doing to x
```

#### Filter

Filter is very similar to Map just like in JavaScript

```text
myList = [2,3,4,5,5]
filtered = filter(lambda x:x < 3, myList
list(filtered)
```

