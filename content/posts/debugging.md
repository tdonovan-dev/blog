---
title: "Debugging"
date: 2023-03-31T10:54:50-03:00
---

This is quick intro to debugging as a software developer.

### What is debugging?
Do you find yourself struggling to figure out why an app you're developing is giving you the wrong value? Do you find yourself writing this a lot in your code? 

```JavaScript
console.log(someVariableThatDoesntSeemToBeWorking)
```

If your answer is 'yes', That's okay. Although checking your console for errors is a very good place to begin searching for answers, logging your variables to the console everytime you have an issue is not a very good practice. You have probably run into an error in your console that may make no sense to you at all.

Software debugging is when you find and fix errors in your programs. These errors, or bugs, can cause a program to behave incorrectly or stop working entirely. Debugging is a necessary part of the software development life cycle and can be a time-consuming task, but is ultimately very important.

### How do I debug?

You should be able to begin debugging in most any integrated development environment (IDE). IDEs provide a range of tools and features that can make debugging more efficient and effective. An IDE, along with a text editor and compiler or interpreter, usually has a debugger.

When you debug in an IDE, you have the ability to set breakpoints. These are points in the code where the debugger will stop the program's execution and allow you to look into the state of the program. This is useful for finding the cause of a bug, and allows you to see the values of variables and examine the flow of code at any specific point.

![debugging in vscode](https://code.visualstudio.com/assets/docs/editor/debugging/log-points.gif)
>source: *code.visualstudio.com*

Debugging your apps is not only limited to writing code itself. You can also place breakpoints in your tests in the same way, although, setup may be specific to whichever testing framework you are using.

### IDE and Browser

There is a lot of documentation and tutorials online to begin debugging in whichever IDE you use. However, a good philosphy to have as a dev, is to always be looking for better tools and expanding what you already know. With this in mind, I recently learned a new, very simple method to debug front-end nodejs applications in your browser itself. 

To begin, write `debugger` wherever you would like your code to stop executing and begin stepping line-by-line.

```JavaScript
// code

debugger

// more code

```

Then, in your terminal write `NODE_OPTIONS="--inspect"` followed by anything that runs nodejs (ex: `npm run dev`). 
Now, when your program reaches the debugger line in execution, your browser will stop. You can open your dev tools and step through the code right in your browser.

### Saving Engineering Hours
Software developers should use tools as much as they can do be better, more productive coders. Similarly, devs should also stay up-to-date on what tools are newly available to them.
