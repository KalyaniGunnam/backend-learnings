# Data Types

In Java, data types specify the type of data that variables can store. (or) A data type is a classification of data which tells the compiler or interpreter how the programmer intends to use the data. Java supports two categories of data types: 
- primitive data types 
-non-primitive (or) reference data types.

### Primitive Data Types : 
Primitive data types represent basic data values and are predefined by the Java language. There are eight primitive data types in Java:
```
(a) numeric type of data:
    - Integer data type : 
        - byte: 8-bit signed integer. → 1 byte
        - short: 16-bit signed integer. → 2 bytes
        - int: 32-bit signed integer. → 4 bytes
        -  long: 64-bit signed integer. → 8 bytes__
    -Floating point data type  :
        - float: 32-bit floating-point number. → 4 bytes
        - double: 64-bit floating-point number. → 8 bytes
(b) boolean type of data:
    - Represents true(1) or false(0). → 1 bit
(c) character type of data:
    - 16-bit Unicode character. → 2 bytes
```

#### Examples:: 
// Primitive data types
byte myByte = 10;
short myShort = 100;
int myInt = 1000;
long myLong = 100000L;
float myFloat = 10.5f;
double myDouble = 10.12345;
char myChar = 'A';
boolean myBoolean = true;


Note : In Java, a wrapper class is a class that wraps a primitive data type within an object. 

Integer: Wraps an int.
Long: Wraps a long.
Float: Wraps a float.
Double: Wraps a double.
Byte: Wraps a byte.
Short: Wraps a short.
Character: Wraps a char.
Boolean: Wraps a boolean

### Non-Primitive (or) Reference Data Types :
Non-Primitive data types refer to objects and are created using classes or interfaces. They store references to objects in memory rather than the actual data. Examples of reference data types include classes, arrays and collections.

#### Examples:
// Reference data types
String myString = "Hello, Java!";
int[] myArray = {1, 2, 3, 4, 5};

# Computer Memory Units :
Computer memory units refer to the units of measurement used to quantify the amount of memory (storage capacity) in a computer system. These units are used to describe the size or capacity of various types of memory components, such as RAM (Random Access Memory), storage devices (hard drives, solid-state drives), and cache memory. Here are some commonly used memory units:
Bit = Binary Digit
1 Nibble = 4 bits
1 Byte = 8 bits
1 Kilo Byte (KB) = 1024 bytes
1 Mega Byte (MB) = 1024 KB
1 Giga Byte(GB) = 1024 MB
1 Tera Byte(KB) = 1024 GB
1 Peta Byte(KB) = 1024 TB

# Default Values For Primitive Data Types :
byte: 0
short: 0
int: 0	
long: 0L
float: 0.0f
double: 0.0d
boolean: false
char: '\u0000' (null character)
