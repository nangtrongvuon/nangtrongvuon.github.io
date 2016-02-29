---
layout: post
title:  Swift - Constant, Variables, Optionals
date:   2016-02-29 9:00:00
---

Thus begins my first post. More will come as I proceed on my journey to mastering Swift.

I think the very basics of programming is that data is stored in constant and variables. When you make a new constant or variable, a spot in the memory is created for that specific data.

```Swift
// Swift
let a = 1
var b = 2

```

In *Swift*, to declare (make) a *constant*, you use "let". You can read that as "let a be 1", as I often do. For *variables*, you use "var". That can also be read as, "variable b is 2".

The difference between a constant and a variable is that, variables can be changed, while constants cannot, as their names imply.

You can provide Swift a *"type annotation"* when you make a constant or variable, so Swift knows what kind of value the constant or variable can store. An example is provided below.

```Swift
// Swift
var a: Int
let b: String
```

This tells Swift that *a* can store an Int. So *a* can now be 100, or 10000, or anything that is an integer. And *b* can store a String, so *b* can be changed to say *"hello world!"*.

You can even do this type annotation stuff for multiple variables at once.

```Swift
var a, b, c: Int
```
This means *a, b, c* are all Integers.

So I think that was simple enough to understand. Let's talk about optionals now.

One of the concepts that really tripped me in the beginning was optionals. As a person who was used to Python and various other programming languages, where the concept of optionals didn't really exist, I was surprised on seeing emotional code. You know, they have things like **!** and **?** behind variable names and methods!

In *Swift*, sometimes, constants and variables may have **!** or **?** behind their names. Something like,

```Swift
let optionalA: Int?
var optionalB: Int!
```

*"Int?"* in Swift terms mean, that constant may not have a value. In programming, if something doesn't have a value, then its value can be called "nil". So optionalA can have no value *(nil)*, or it can have an *Int* (Integer, kinda like whole numbers.)

*"Int!"* in Swift terms mean, this variable, *optionalB* may be nil, but I know it will never be nil. So, *optionalB* will always have a value. It is essentially the same as variables in many other programming languages. However, if Swift catches you using ! for a variable that is nil, your program will crash, so be careful.

In Swift, to safely use the non-nil value (people call this, *unwrapping*), you use what is called, *optional binding*. That's kind of fancy terms for this:

```Swift
// Tell Swift that optionalA can store an Integer
var optionalA: Int?

if let numberInOptionA = optionalA {
  // Prints the value of numberInOptionA to the console
  print(\(numberInOptionA)
}
```

**If**, *there is a value in optionalA*, then *take that value and store it in a constant called*, **numberInOptionA**. If there is no value in optionalA, meaning that optionalA is nil, then the if code doesn't execute.

By the way, that *"if"* thing is a staple for programming, called **control flow**.  I'll make a blog post on that later. I hope that was enough for this post.

If you have any questions, I'll try to answer it for you, from one learner to another. My info can be found in the *about* tab of this page.

See you later,
*Nắng Trong Vườn*
