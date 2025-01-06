# Packages in Java 
Think of packages in Java like folders on your computer. Just like you use folders to organize your files, Java uses packages to organize its classes and make your programs neat and easy to manage.

For example:

Imagine you’re organizing a school project. You might have a folder for Math, another for Science and another for English. Each folder has related files.
Similarly, in Java, a package can have related classes grouped together.

# Why Do We Use Packages?
- Organizing Code: Helps keep related classes together so you can find and manage them easily. For Example: Classes for user details go in one package, while classes for database operations go in another.
- Avoiding Name Conflicts: If two people create a class with the same name, packages help avoid confusion by keeping them in different folders (packages).
- Reusability: You can use pre-existing Java packages (like tools provided by Java itself) instead of writing everything from scratch. For Example: The java.util package has ready-made tools like lists and maps for managing data.

# How Do You Create a Package?
Use the package keyword at the top of your Java file to define which package the class belongs to.
```
package mypackage;

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello from mypackage!");
    }
}

```
Save this file in a folder matching the package name (mypackage).

# Real-Life Example:
- Without Packages: All your clothes are dumped into one drawer. It's hard to find socks or shirts when you need them.
- With Packages: Clothes are organized into different drawers—one for socks, one for shirts and one for pants. Everything is easy to find!

# Different Types of Packages
In Java, packages are broadly categorised into two types: built-in(or) standard packages and user-defined packages.
## 1. Built-in Packages:
Java provides a rich set of built-in packages that come with JDK.These packages contain wide variety of classes and interfaces(this will be covered in future classes) that provides essential functionalities for java programming. In simple terms, these are pre-written collections of useful code that Java gives you. Instead of writing everything from scratch, you can "borrow" these tools to do things faster and more efficiently. Some of the most commonly used built-in packages include,
- **java.lang:** Contains fundamental classes that are automatically imported into every Java program.
Example: Want to convert a number to a string? Use tools from java.lang.

- **java.util:** Contains utility classes such as collections,date and time facilities, random number generation and more.
Example: You can use ArrayList to store a list of items.

- **java.io:** Provides classes for input and output, like reading a file or saving data.
Example: Want to write data to a file? Use tools from java.io.

-**java.net:** Contains classes for networking applications, like connecting to a website or sending data over the internet.
Example: Want to download a file from the internet? Use java.net.

-**java.sql:** Used for working with databases.
Example: Want to fetch data from a table in MySQL? Use java.sql.

Similarly, there are many more. We will explore them as we progress..

### I would like to comapre this with a real-life analogy

Imagine you want to bake a cake. Instead of making everything from scratch (like grinding your own flour or extracting sugar from plants), you use ready-made ingredients from the store. Built-in packages are like those ready-made ingredients—they make your programming life easier by giving you tools that are already prepared!

## 2. User-Defined Packages:
These packages are created by the developers to organise their own classes and interfaces in a logicalk manner.Thse packages help manage the codebase efficiently, avoid naming conflicts and improve maintainability.
