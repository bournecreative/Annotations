# List Comprehensions

Similar to how map and filter work but there is a major difference in how these functions iterate through items. When map and filter iterate through a list, they iterate through list, incrementally which results in less memory being used. List comprehensions iterate through the entire list and return the entire result. Consequently this results in more memory being used.

```text
// list comprehensions generates a new list
// you define a list comprehension within brackets
myList = [1,2,3]

listComp = [x**2 for x in myList] //for every value in the list square it
print(listComp)
```



