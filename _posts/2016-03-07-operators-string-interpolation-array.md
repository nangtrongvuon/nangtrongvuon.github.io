---
layout: post
title:  Operators, String Interpolation, Arrays
date:   2016-03-07 3:00:00
---
Welcome to the next segment of my posts.

# Operators
You can make Swift, or any programming language in general, do cool things.

```
var a = 10
b = a + 2
c = a - 2
d = a * 2
e = a / 2
print(b, c, d, e); // that'd say 12, 8, 20 and 5, respectively.
```

If you know math, this should be straightforward. You can even do squared calculations.

There are also comparison operators, like >, <, <=, >=, ==.
In programming, however, do not use **"="** as an equality operator. It is reserved for assigning variables and constants. Use **"=="** instead.

# String Interpolation

By the way, some operators work with strings too.
```
var test = "Hello "
var test2 = " world!"
var test3 = test + test2
print(test3) // "Hello world!"
```

If you have a variable or constant of some kind and you want to display it in a String, use the **String Interpolation** technique. It sounds scary, but all you have to do is:
```
var thing = 10
print(Thing is \(thing))
```

You put the variable/constant that you want to be displayed in the string in parentheses "()" and add a backslash character - **"\"**.
Anything between the string interpolation can be an operator. So you can do calculations like:
```
var age = 10
print (You are \(age) years old. You will be \(age+1) next year.
```

Swift is smart like that.

# Arrays
Arrays are collections of data. They usually look like this:

```
var array = ["a", "b", "c"]
```
Brackets are used to mark the start and end of an array, and each item is seperated by a comma.
You can access items in arrays by typing the array name along with brackets and the index of the item you want.

However, computers count arrays from 0 and not 1. So, in an array of 5 items, the max index is 4.

```
var array = ["a", "b", "c"]
print array[0] // "a"
```
To create your own array, type the name of the array, and then wrap its type (the type of its contents) in brackets, then finally put parentheses after that.

```
var array: [String]()
```

If you are coming from another language, Swift doesn't let you declare the array first and then add things to it later.

```
var newArray: [String]
newArray[0] = "a" // doesn't work
```

When you use *var array: [String]*, Swift simply knows that there's going to be an array named **newArray** that will store strings, and doesn't actually create it
until later. To make the array, use the technique(syntax) above.

You can also use operators on arrays. You can merge 2 arrays with "+":

```
var array1 = ["a", "b", "c"]
var array2 = ["d", "e", "f"]
var array3 = array1 + array2
print(array3) // ["a", "b", "c", "d", "e", "f"]

```

I think that should be enough for now.
See you later,
*Nắng Trong Vườn*
