# Thumb Rules For Writing Any Java Program

## 1. Everything Happens in a Class
- In Java, whatever you write must be inside a class.
- Think of a class as a box where all your program’s instructions are stored.
- You create a class using the class keyword. For example:

class TestProgram{

}

## 2. Classes Hold Variables and Methods
- A variable is like a container that stores information (e.g., a number or a name).
- A method is a set of instructions that do something when you run your program.

## 3. Use Curly Braces for Grouping
- If your program has multiple instructions, you must wrap them inside { } curly braces. These braces group the instructions together.

## 4. Main Method is the Entry Point
- To run a Java program, you must have a main method.
- Think of the main method as the starting point where your program begins. For example:

class TestProgram{
    public static void main(String[] args){
        system.out.println("Hello, World");
    }
}

## 5. Class Names Should Start with a Capital Letter
- It’s a good habit to name your class starting with a capital letter (e.g., TestProgram instead of testProgram). This makes your code more readable.

## 6. Compile and Run the Program
Step 1: Compile the Code
- Java code is written in a .java file (e.g., Test.java).
- Use the Java compiler (javac) to convert your code into a language the computer understands.
- This process creates a .class file (e.g., Test.class). This file contains the bytecode.
- Command to Compile: javac Test.java
Step 2: Run the Program
- After compiling, use the java command to execute the program.
Command to Run: java TestProgram

## 7. Example

If you write this program:
class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}

- Save it as HelloWorld.java.
- Compile it: javac HelloWorld.java
- Run it: java HelloWorld

You’ll see: Hello, World!
