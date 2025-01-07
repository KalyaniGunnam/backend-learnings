# Type Conversion:
In Java, Type conversion is the process of converting one data type into another. In Java, to store the data we have data types. These data types help us in storing different types of data. So to convert one type of data into another type of data we have the process and that is called type conversion.  
This is introduced because java by default can’t do all the conversions. As a user we need to do some conversions explicitly. Which means we have to tell the java  explicitly to perform these conversions.That is why java introduced this type conversion.

# Different Types of type conversions:
There are two types of type conversions:
- Implicit conversion or Automatic conversion or widening or upcasting
- Explicit conversion or Manual conversion or narrowing or downcasting

In industry sometimes type conversion is also called type casting. They both are almost similar. When converting primitive data types, it is called type conversion. When converting non-primitive data types, it is referred to as type casting.

### Implicit conversion:
Implicit conversion occurs automatically when the compiler converts a smaller data type to a larger data type. This process is also known as widening or upcasting because it moves from a less precise to a more precise data type without any loss of information.

Common Implicit Conversions in Java:
```
byte →  short, int, long, float, double
short → int, long, float, double
char → int, long, float, double
int → long, float, double
long → float, double
float → double
```

### Explicit conversion:
Explicit conversion requires the programmer to manually convert one data type to another. This is also known as narrowing or downcasting because it involves converting from a larger data type to a smaller data type, which may result in a loss of information.

Common Explicit Conversions in Java:
```
double → float, long, int, short, byte
float → long, int, short, byte
long → int, short, byte
int → short, byte
char → byte, short
short → byte
```

# Example 1:
```
package practice.typecasting;

public class TypeCastingPractice {
   public static void main(String[] args) {
       byte a = 10; // -128 to 127
       short b = 20;
       int c = 30;
       long d = 40;
       float e = 50.15F;
       double f = 60.60;


       //Implicit Conversion
        b = a;  // byte to short
        c = a;  // byte to int
        d = a;  // byte to long
        e = a;  // byte to float
        f = a;  // byte to double
        System.out.println(a + "\n" + b +"\n" + c + "\n" + d + "\n" + e +"\n" + f); // Output: a = 10 (byte)
                                                                                        b = 10 (byte to short)
                                                                                        c = 10 (byte to int)
                                                                                        d = 10 (byte to long)
                                                                                        e = 10.0 (byte to float)
                                                                                        f = 10.0 (byte to double)


        c = b; // short to int
        d = b;  // short to long
        e = b;  // short to float
        f = b;  // short to double
        System.out.println(a + "\n" + b +"\n" + c + "\n" + d + "\n" + e +"\n" + f); // Output: a = 10 (unchanged from previous)
                                                                                        b = 20 (short, assigned earlier)
                                                                                        c = 20 (short to int)
                                                                                        d = 20 (short to long)
                                                                                        e = 20.0 (short to float)
                                                                                        f = 20.0 (short to double)


       //Explicit Conversion
       a = b; // short to byte
       System.out.println(a);  <--  This will cause a compile-time error because you are trying to assign a short to a byte without explicit casting.
        a = (byte) b; // Explicit cast
       System.out.println(a); // Output: 20.  After explicit casting to byte, a = 20 because the value is within the range of byte (-128 to 127).


       a = (byte) f;
       System.out.println(a); // Output: 60. Explicit casting truncates the fractional part (60.60 becomes 60) and then wraps it to fit within the byte range: 60 is within the range, so a = 60.
       a = (byte) e;
       System.out.println(a); // Output: 50. Explicit casting truncates the fractional part (50.15 becomes 50) and assigns it to a.


       c = (int) f; //Output: 60. Explicit casting truncates the fractional part (60.60 becomes 60) and assigns it to c.
       System.out.println(c);
   }
}
```
# Limitations:
1.
```
package practice.typecasting;


public class TypeCastingPractice {
   public static void main(String[] args) {
       byte a = 10; // -128 to 127 (256) → 0,1,2,...127,128,-127,-126,....0,1,2,.. 
       short b = 20; // -32768 to 32767 (65536) →  0,1,2,...32767,32768 ,-32767,-32766,....0,1,2,..
       int c = 300;
       long d = 40;
       float e = 50.15F;
       double f = 60.60;


       a = (byte) c;
       System.out.println(a); // Output: 44
   }
}
```
When converting a larger data type to a smaller one, Java doesn't throw an error. Instead, it performs a type conversion where the value is truncated to fit within the range of the smaller data type. This process results in a value that might seem random but is actually predictable based on the sizes of the data types involved.

byte ranges from -128 to 127, meaning it can hold 256 different values. int has a much larger range, but we're specifically looking at the value 300. When you cast an int (300) to a byte, Java takes the value and fits it into the byte's range. The value 300 exceeds the byte's maximum value (127). So, Java uses the modulo operation to fit it within the byte's range.

Java uses the formula: Result = Value % Range
For byte, the range is 256 (from -128 to 127).
Calculating  >>>>  300 % 256 gives us 44.

2. The boolean values cannot be cast to any other data type and vice versa also not possible.
Example: 
boolean boolValue = true; // Trying to cast boolean to int (invalid) 
int intValue = (int) boolValue; // Compilation error: incompatible types

3. 
```
Example:
package practice.typecasting;


public class TypeCastingPractice {
   public static void main(String[] args) {
       byte a = 10; // -128 to 127 (256)
       short b = 20;
       int c = 300;
       long d = 40;
       float e = 50.15F;
       double f = 60.60;


       //byte a2 = a + a; // a+a is considered as int even though we provide byte values
       byte a2 = (byte) (a + a); // Explicit cast required
       System.out.println(a2);// Output: 20
   }
}
```
This is called Automatic type promotion. When performing arithmetic operations, the operands are automatically promoted to a common type before the operation is carried out. This ensures that the operations are performed consistently and without loss of precision.
In Java, arithmetic operations involving byte, short, or char are automatically promoted to int before the operation is performed.
If one of the operands is of a type wider than int, such as long, float, or double, the other operand is promoted to the wider type.
