# What Is A Class

A Class is a blueprint for creating objects. Every class contains two things - variables and methods.

### Analogy

I will compare this with one analogy for better understanding. Imagine you’re in a toy factory. The factory has a blueprint for making a Dog toys. This blueprint (class) specifies -
- what every Dog toy should have (its properties)  - E.g: breed, size, color
- what it can do (its actions) - E.g: bark, wag tail 

In the same way, a Java class defines the structure (variables) and behavior (methods) for objects.

# Defining A Class

In Java, a class is defined using the class keyword. Each class must have a name as a means of identification. In a project, we can have multiple classes and each class should have a unique name to distinguish it from others. This unique identification, the class name, serves as a reference point for utilising or interacting with the class in the future.

# Components Of A Class

Every class in Java contains two main components: Variables and Methods.

### 1. Variable

Variables represent the state or data of an object. They define the characteristics or properties that objects of the class will possess. Variables are declared within the class and can have various data types.  There are two different types of variables: 
- instance variables (fields that belong to each instance of the class) 
- static variables (fields that belong to the class itself).

### 2. Method

Methods define the actions that objects of the class can perform. They represent the operations that can be performed on the object's state. Methods are declared within the class and can have various access modifiers and return types. There are two different types of methods:
- instance methods (methods that operate on instance variables)
- static methods (methods that belong to the class itself).

```
package com.mypractice;

public class Dog {
	public String breed = "German Shepard";
	public int height = 30; // in cm
	public int weight = 50; // in kg
	
    public static void main(String[] args) {
		Dog dog = new Dog();
		System.out.println("Breed: " + dog.breed);
	}
}
```