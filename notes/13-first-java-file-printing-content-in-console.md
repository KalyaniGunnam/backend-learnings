# Printing Random Stuff in Java

## Introduction
In this section, we will start working directly with Java code. As we discussed before, every Java program requires a class and a `main` method, which is the entry point to the execution of the program. Let's begin by writing a simple program that prints text to the console.

## Setting Up the Program
We start by defining a class called `PrintingRandomStuff`. This class will contain the `main` method, which is the starting point of our program:

```
class PrintingRandomStuff {
    public static void main(String[] args) {

    }
}
```
In this structure:

- **PrintingRandomStuff** is the class name.
- **public static void main(String[] args)** is the method where the program starts executing.

## Running the Program in IntelliJ IDEA
I am using **IntelliJ IDEA** as my Integrated Development Environment (IDE), we can run the program by clicking on the run triangle icon at the top. Once the program executes, the console will display:
```
Process finished with exit code 0
```
This indicates that everything is working fine.

## Printing Text to the Console
To display something on the console in Java, we use the **System.out.print()** method. The content you want to display should be enclosed in quotation marks **(" ")**. For example, to print "I like pizza", the code will look like this:
```
class PrintingRandomStuff {
    public static void main(String[] args) {
        System.out.print("I like pizza!");
    }
}
```

## Expected Output
When you run the program, the output displayed on the console will be:
```
I like pizza!
```
This is a simple way to print text to the console in Java.

# Printing Multiple Lines in Java: Fixing Output Formatting

## Problem Overview
Let's extend our program and print two sentences on separate lines. Initially, we write the following code:

```
public class PrintingRandomStuff {
    public static void main(String[] args) {
        System.out.print("I like pizza!");
        System.out.print("It’s really delicious!");
    }
}
```

## Obtained output 
```
I like pizza!It’s really delicious!
```

This output isn't as expected because the two sentences are printed on the same line, without a break. We want the output to appear on two separate lines, like this:

```
I like pizza!
It’s really delicious!
```

# Solution
There are two ways to fix this:
- **1. Using \n for a line break**

The \n is a special character known as a newline character. It can be inserted at the end of the string to indicate a line break.

```
public class PrintingRandomStuff {
    public static void main(String[] args) {
        System.out.print("I like pizza!\n");
        System.out.print("It’s really delicious!");
    }
}
```
The \n after the first sentence will insert a line break, making the output appear on two separate lines.

- **2. Using System.out.println()**

The other approach is to replace **System.out.print()** with **System.out.println()**. The println() method automatically moves to a new line after printing the content, so you don’t need to manually insert \n.
```
public class PrintingRandomStuff {
    public static void main(String[] args) {
        System.out.println("I like pizza!");
        System.out.println("It’s really delicious!");
    }
}
```
By using System.out.println(), the program will print each sentence on a new line automatically.
```
I like pizza!
It’s really delicious!
```

# Conclusion: `System.out.print()` vs `System.out.println()`

In Java, both `System.out.print()` and `System.out.println()` are used to print text to the console, but they behave differently when it comes to handling line breaks:

1. **`System.out.print()`**:
   - It prints the specified content but **does not move to a new line** after the output.
   - You can manually add a line break by inserting `\n` at the end of the string, which will force the output to the next line.

2. **`System.out.println()`**:
    - It prints the content and automatically moves to a new line after the output.
    - This is the simplest and most commonly used method when you want each statement to be printed on a new line.
