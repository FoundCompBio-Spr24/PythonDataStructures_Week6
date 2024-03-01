# Python Data Structures

## Lists

- We've now covered the simple variable types in Python: integers, floats, strings, and bools.
- However, there are several more complex types of variables that allow us to store and access multiple values.
- Perhaps the most versatile and common of these more complex types are lists.
- Lists are always specified using square brackets - `[]`
- Lists can contain an arbitrary number and type of simpler variables, but we often want to use only one type in a list so as not to get confused.
    - `listOfNums = [1,2,3,4]`
    - `listOfFloats = [3.14, 2.0, 12.3]`
    - `listOfStrings = ["Ecology", "Evolution", "Systematics"]`
    - `listOfBools = [True, False, False, True]`
- Even after they are created, lists can be modified. Individual elements can be added using the append method():
    - `listOfNums.append(5)` - Examine list after executing
    - `listOfStrings.append("Neurobiology")`
- Elements can be removed using a few different methods.
    - Try `listOfFloats.pop()` - What is returned? And what does the list look like now?
    - You can remove specific values from a list, regardless of their position, by using the `remove(<VALUE>)` method. What happens when you execute `listOfBools.remove(False)`? How does the list change?
- Lists can contain lists as elements. For instance, try this:
    - `newList = []`
    - `newList.append([1,2,3])`
    - `newList.append([4,5,6])`
    - `newList.append([12,13,14])`
- But you can also add all the _individual elements_ of one list to another. Try this:
    - `newList = [1,2,3]`
    - `newList.extend([4,5,6])`
    - `newList.extend([12,13,14])`
    - How does `newList` differ from what you got when you used `append()`?
- You can view or extract parts of a list by using indices and "slicing" the list (just remember that python starts counting at 0!)
    - `newList[4:7]` - What values are returned? How do these relate to the indices you provided?
- You can also extract every n-th element of a list using notation like this:
    - `newList[::2]` - What values are returned now?
    - `newList[2:8:2]` - How about now?
- You can also alter individual elements of lists by using indices
    - `newList`
    - `newList[2] = 100`
    - `newList`

## `for` loops
  
- One of the nicest things about Python is the relationship between lists and `for` loops
- If you have an existing list, you can quickly iterate across all of its elements using this syntax:

```
for num in newList:
    print("This number is: %d" % num)
```
            
- If you still want to iterate over a series of integers, you can use the range() function.

```
for num in range(10):
    print("This number is: %d" % num)
```

## A note about "copying objects"

- Try this:
    - `firstNum = 2`
    - `secondNum = firstNum`
    - `firstNum = 5`
    - `firstNum`
    - `secondNum`
- Now try this:
    - `firstList = [1,2,3]`
    - `secondList = firstList`
    - `firstList.extend([4,5,6])`
    - `firstList`
    - `secondList`

## Tuples

- Tuples are like lists, but they're not mutable (can't be changed)
- Tuples are instantiated using parentheses - `()`
- Try this:
    - `myTuple = (1,2,3)`
    - `myTuple`
    - `myTuple[1]`
    - `myTuple[1] = 5`

## While loops

- Sometimes we want to do something repetitively, but we don't know ahead of time how many times we need to repeat it (as in a `for` loop.
- In these cases, we can use a `while` loop. A `while` loop will continue to do something until a certain condition is no longer satisfied.

```
num = 0
while num < 10:
    print(num)
    num += 1
```

- WARNING - You need to make sure to update variables such that the condition will eventually be satisified. If you don't, you could create an infinite loop!

## Dictionaries

- Dictionaries are incredibly useful for storing pairs of things - known as "keys" and "values"
- They don't store these pairs in a particular order, like lists do, but they make looking up values from keys much faster.
- The keys and values can each be different types of variables
- To create a new dictionary, you can use this syntax:
    - `myDict = {"keyOne":"valueOne", "keyTwo":"valueTwo"}`
- To look at the methods available for dictionaries, try this:
    - `dir(myDict)`
- You can access a value, as long as you know its key, either of these ways:
    - `myDict.get("keyOne")`
    - `myDict["keyOne"]`
- You can change a value using its key, this way:
    - `myDict["keyOne"] = <NEW_VALUE>`
- You can add a new key/value pair using the update method:
    - `myDict.update({<NEW_KEY:NEW_VALUE})`
