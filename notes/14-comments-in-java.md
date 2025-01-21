# Java Comments

In Java, comments are used to add explanatory notes to your code. These comments are ignored by the Java compiler, meaning they do not affect the execution of the program. Comments are useful for documenting the code, explaining logic, and making the code more understandable for others (or for yourself in the future).

There are three types of comments in Java:

## 1. Single-Line Comments
Single-line comments are used to write short, inline explanations. They begin with `//`, and everything after `//` on that line will be considered a comment.

**Syntax:**
```
// This is a single-line comment
```


## 2. Multi-Line Comments
Multi-line comments are used for longer explanations or to comment out multiple lines at once. They begin with /* and end with */. Everything between these markers is treated as a comment.

**Syntax:**
```
/* This is a multi-line comment.
   It can span multiple lines. */
```
*Multi-line comments are useful when you need to write a more detailed explanation or temporarily disable sections of code during development*

## 3. Javadoc Comments
Javadoc comments are a special type of comment used to generate documentation for Java classes, methods and fields. They start with /** and end with */. These comments can include tags such as @param, @return, and @throws to provide structured documentation.

*Javadoc comments are used to generate HTML documentation for your project using the javadoc tool. This documentation is often used to provide detailed descriptions for API documentation.*