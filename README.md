# java  
## data type  
In Java, types are classifications of data that define the kind of values that variables can hold and the operations that can be performed on those values. Java has two categories of types: primitive types and reference types.

**1)Primitive Types:**
Primitive types represent basic data types built into the Java language. They are not objects and do not have methods. There are eight primitive types in Java:  

byte: 8-bit signed integer   
short: 16-bit signed integer  
int: 32-bit signed integer  
long: 64-bit signed integer  
float: 32-bit floating point number  
double: 64-bit floating point number  
char: 16-bit Unicode character  
boolean: Represents true or false values  

**2)non-Primitive(refrence) Types:**  
Reference types are class types, interface types, and array types. They refer to objects in memory and can have methods and fields. Reference types are created using class or interface definitions, and variables of reference types hold references (memory addresses) to objects.   
 ## string ex   
 ```py
public class StringExample {
    public static void main(String[] args) {
        // Creating string objects
        String str1 = "Hello, ";
        String str2 = "World!";
        String str3 = "Java";

        // Concatenation
        String combinedStr = str1 + str2;
        System.out.println("Concatenated String: " + combinedStr);

        // Length of the string
        int length = combinedStr.length();
        System.out.println("Length of the String: " + length);

        // Accessing characters at specific index
        char charAtIndex = combinedStr.charAt(7);
        System.out.println("Character at index 7: " + charAtIndex);

        // Substring
        String substring = combinedStr.substring(0, 5);
        System.out.println("Substring from index 0 to 4: " + substring);

        // Splitting string
        String[] parts = combinedStr.split(", ");
        System.out.println("Splitting the string: ");
        for (String part : parts) {
            System.out.println(part);
        }

        // Checking if a string contains a specific substring
        boolean containsJava = combinedStr.contains("Java");
        System.out.println("Contains 'Java': " + containsJava);

        // Converting string to uppercase
        String upperCaseStr = combinedStr.toUpperCase();
        System.out.println("Uppercase String: " + upperCaseStr);

        // Converting string to lowercase
        String lowerCaseStr = combinedStr.toLowerCase();
        System.out.println("Lowercase String: " + lowerCaseStr);
    }
}
```
**OUTPUT**
```py
Concatenated String: Hello, World!
Length of the String: 13
Character at index 7: W
Substring from index 0 to 4: Hello
Splitting the string:
Hello
World!
Contains 'Java': false
Uppercase String: HELLO, WORLD!
Lowercase String: hello, world!

```

## Arrays ex  
```py
public class ArrayExample {
    public static void main(String[] args) {
        // Creating an array of integers
        int[] numbers = {10, 20, 30, 40, 50};

        // Accessing elements by index
        System.out.println("Element at index 2: " + numbers[2]);

        // Modifying elements
        numbers[3] = 45;
        System.out.println("Modified element at index 3: " + numbers[3]);

        // Length of the array
        int length = numbers.length;
        System.out.println("Length of the array: " + length);

        // Iterating over elements using for-each loop
        System.out.println("Elements of the array:");
        for (int number : numbers) {
            System.out.print(number + " ");
        }
        System.out.println();

        // Sorting the array
        java.util.Arrays.sort(numbers);
        System.out.println("Sorted array:");
        for (int number : numbers) {
            System.out.print(number + " ");
        }
        System.out.println();

        // Searching for an element
        int index = java.util.Arrays.binarySearch(numbers, 30);
        System.out.println("Index of element 30: " + index);
    }
}
```

**OUTPUT**
```py
Element at index 2: 30
Modified element at index 3: 45
Length of the array: 5
Elements of the array:
10 20 30 45 50 
Sorted array:
10 20 30 45 50 
Index of element 30: 2

```

## casting  

In Java, casting refers to the process of converting a value of one data type into another data type. There are two types of casting: widening (implicit) casting and narrowing (explicit) casting.

**1) Widening (Implicit) Casting:**
Widening casting is the conversion of a value from a smaller data type to a larger data type. It is also known as automatic type conversion because it is done automatically by the Java compiler. Widening casting does not result in loss of precision.  
```py
public class WideningCastingExample {
    public static void main(String[] args) {
        int intValue = 10;
        double doubleValue = intValue; // Widening casting from int to double
        
        System.out.println("int value: " + intValue);
        System.out.println("double value: " + doubleValue);
    }
}

```
**output**  
```py
int value: 10
double value: 10.0

```
**2) Narrowing (Explicit) Casting::**   
Narrowing casting is the conversion of a value from a larger data type to a smaller data type. It is also known as manual type conversion because it requires an explicit cast operator. Narrowing casting may result in loss of precision if the value being converted cannot be represented accurately in the target data type.  
```py
public class NarrowingCastingExample {
    public static void main(String[] args) {
        double doubleValue = 10.5;
        int intValue = (int) doubleValue; // Narrowing casting from double to int
        
        System.out.println("double value: " + doubleValue);
        System.out.println("int value: " + intValue);
    }
}

```
**output**

```py
double value: 10.5
int value: 10
```

## Taking input   
```py
import java.util.Scanner;

public class InputExample {
    public static void main(String[] args) {
        // Create a Scanner object to read input from the console
        Scanner scanner = new Scanner(System.in);

        // Prompt the user to enter their name
        System.out.print("Enter your name: ");
        String name = scanner.nextLine(); // Read a line of text input

        // Prompt the user to enter their age
        System.out.print("Enter your age: ");
        int age = scanner.nextInt(); // Read an integer input

        // Display the input received from the user
        System.out.println("Hello, " + name + "! You are " + age + " years old.");

        // Close the Scanner object to release resources
        scanner.close();
    }
}
```
## switch  
--In Java, the switch statement is a control flow statement used to select one of many code blocks to be executed based on the value of an expression. It provides a convenient way to execute different blocks of code based on the value of a single variable or expression.
```py
switch (expression) {
    case value1:
        // Statements to be executed if expression equals value1
        break;
    case value2:
        // Statements to be executed if expression equals value2
        break;
    // More cases can be added as needed
    default:
        // Statements to be executed if none of the above cases match
}

```

## exception handling  
Exception handling in Python is a mechanism to deal with runtime errors, also known as exceptions, gracefully. Exceptions occur when something unexpected happens during the execution of a program, such as division by zero, trying to access a file that does not exist, or attempting to access an index outside the bounds of a list.   


In Python, the equivalent of try and catch in other languages like Java is achieved using the try and except blocks.  

**try block:** The try block is used to enclose the code that might raise an exception. It allows you to specify code that you want to monitor for exceptions.  

**except block:** The except block is used to handle exceptions that occur within the try block. If an exception occurs, control is transferred to the corresponding except block. You can have multiple except  
 blocks to handle different types of exceptions.  

 ```py
try:
    # Code that might raise an exception
    # For example, division by zero
    result = 10 / 0
except:
    # Handle the exception
    print("An error occurred")
```
# oops  
## classes  and Objects real life example  
--a class is like a recipe, and an object is like the dish prepared using that recipe.
## classes  
In Java, a class is a blueprint or template for creating objects. It defines the attributes (fields) and behaviors (methods) that objects of that class will have.   
```py
public class MyClass {
    // Fields (instance variables)
    int x;
    String name;

    // Constructor
    public MyClass(int x, String name) {
        this.x = x;
        this.name = name;
    }  
    // Method
    public void display() {
        System.out.println("x: " + x + ", name: " + name);
    }
}
```
--In Java, the "this" keyword is a reference to the current instance of the class. It is primarily used to differentiate between instance variables and   
parameters or local variables with the same name within a class.   
## objects
An object is an instance of a class, meaning it is a specific realization of the class blueprint.   
An object is created using the new keyword followed by the class name and parentheses (optional if no arguments are passed to the constructor).  
It represents a specific instance of a class, with its own unique state and behavior.  
Multiple objects can be created from the same class blueprint.  
```py
public class Main {
    public static void main(String[] args) {
        // Creating objects of MyClass
        MyClass obj1 = new MyClass(10, "Alice");
        MyClass obj2 = new MyClass(20, "Bob");

        // Accessing fields and calling methods of objects
        System.out.println("Object 1:");
        obj1.display();
        System.out.println("Object 2:");
        obj2.display();
    }
}
```
--In Java, the new keyword is used to create new instances (objects) of classes. It dynamically allocates memory for the object and initializes its  
fields using the constructor of the class  

**Output**  
```py
Object 1:
x: 10, name: Alice
Object 2:
x: 20, name: Bob

```

## packages --  
are set of code used for reusablity purpose.  
**types**  
1)built in (ex- 'import.java.util.*;')
2)user define(used can define by describing packages. and can impport it later)

#access  modifiers
# getter and setter

