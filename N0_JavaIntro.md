Features of Java


We will discuss the few outstanding features of Java that encourage
developers to write their application and software using Java programming. Using Java, we can develop the complete application and software. Here are
the features of Java programming language:

Platform independent: Java is platform independent; it means we can build the code at once and then deploy and run in any machine or server.

Scalability: Java is an object-oriented programming language, which makes the code modular, scalable, and easy to use and write.

Library: Java has a very huge open-source library available in the market. Since it is open source and free program, anyone can contribute to create java library. These libraries later can be used by developersto write their code.

Development for all device: It supports all kinds of development for all platforms. We can develop desktop, web, and mobile applications using Java.


Open source JDK: Java is open source. A user can download the JDKfrom the official site and use it. A student or developer of Java need not pay anything to use Java. An individual developer or group of developers may contribute as well in JDK to build new classes and methods.


Easy: Java is easy to learn and use. Many books and online materials are available to study Java language.


Development tool: Some excellent IDEs are available for Java developers such as Eclipse, NetBeans, and IntelliJ. These tools have
IntelliSense that keep providing hints to developers to complete the syntax and statement of code


---

Day1 ---

Literals, Assignments & Variables


---
# 🔹 1. **Variables in Java**

A **variable** is a **named memory location** that stores a value which can change during program execution.
It’s like a container holding data.

### Syntax:

```java
datatype variableName = value;
```

### Example:

```java
int age = 25;       // integer variable
String name = "Aman";  // string variable
double salary = 55000.50; // decimal variable
```

---

# 🔹 2. **Literals in Java**

A **literal** is a fixed value directly written in the code.
When you assign a constant value to a variable, that value is called a **literal**.

### Types of Literals:

1. **Integer Literals** → `10`, `-5`, `1000`

   ```java
   int x = 10;
   ```
2. **Floating-Point Literals** → `3.14`, `2.5e3`

   ```java
   double pi = 3.14;
   ```
3. **Character Literals** → `'A'`, `'9'`

   ```java
   char grade = 'A';
   ```
4. **String Literals** → `"Hello World"`

   ```java
   String msg = "Welcome!";
   ```
5. **Boolean Literals** → `true`, `false`

   ```java
   boolean flag = true;
   ```
6. **Null Literal** → `null` (represents no object)

   ```java
   String data = null;
   ```

⚡ **So:**

* `"Hello"` is a **literal**
* `msg` is a **variable**
* `msg = "Hello";` is an **assignment**

---

# 🔹 3. **Assignment in Java**

The **assignment operator (`=`)** assigns a value (literal, expression, or another variable) to a variable.

### Example:

```java
int a = 10;        // assign literal 10
int b = a;         // assign value of variable a
int c = a + b;     // assign result of expression
```

✅ **Important**:

* `=` in Java means **assignment**, not equality.
* Equality comparison is `==`.

---

# 🔹 Putting It All Together

```java
public class Example {
    public static void main(String[] args) {
        // Literals
        int num = 50;             // 50 is integer literal
        double rate = 99.99;      // 99.99 is floating literal
        char grade = 'A';         // 'A' is char literal
        boolean status = true;    // true is boolean literal
        String name = "Aman";     // "Aman" is string literal

        // Assignment examples
        int x = num;              // assign variable value
        int y = x + 5;            // assign expression result

        // Printing variables
        System.out.println("Name: " + name + ", Grade: " + grade);
        System.out.println("x = " + x + ", y = " + y);
    }
}
```

---

# 🔑 Summary

* **Variable** → named memory location (container).
* **Literal** → actual fixed value (data).
* **Assignment** → process of putting a value (literal/expression) into a variable using `=`.

---


Perfect 👌
Let’s carefully break down **Passing Variables to Methods in Java**.

---

# 🔹 1. Concept

When you call a method in Java, you can **pass values (variables)** to it as **arguments**.
The method receives them as **parameters**.

👉 Think of it as:

* **Arguments** → actual values you send.
* **Parameters** → placeholders that receive those values inside the method.

---

# 🔹 2. Types of Passing in Java

Java **always passes arguments by value** (not by reference).
But the behavior looks different depending on whether the variable is **primitive** or **object**.

---

## ✅ (a) Passing **Primitive Data Types**

* When you pass a primitive (like `int`, `double`, `boolean`), a **copy** of the value is given to the method.
* Changes inside the method **do not affect the original variable**.

### Example:

```java
public class PassPrimitive {
    public static void changeValue(int x) {
        x = 50;   // changes only local copy
    }

    public static void main(String[] args) {
        int num = 10;
        changeValue(num);
        System.out.println("num = " + num); // Output: 10 (unchanged)
    }
}
```

---

## ✅ (b) Passing **Objects**

* When you pass an object, the **reference (memory address)** is passed **by value**.
* So both the method parameter and the original variable point to the **same object**.
* If you change the object’s fields, it **affects the original object**.

### Example:

```java
class User {
    String name;
}

public class PassObject {
    public static void changeName(User u) {
        u.name = "Updated";   // modifies object data
    }

    public static void main(String[] args) {
        User user = new User();
        user.name = "Aman";

        changeName(user);
        System.out.println("Name = " + user.name); // Output: Updated
    }
}
```

---

## ✅ (c) Passing **Immutable Objects** (like `String`)

* Special case: `String` is immutable in Java.
* Even though it’s an object, modifying it inside a method doesn’t affect the original.

### Example:

```java
public class PassString {
    public static void changeString(String s) {
        s = "Changed";   // new object, doesn’t affect original
    }

    public static void main(String[] args) {
        String text = "Original";
        changeString(text);
        System.out.println("text = " + text); // Output: Original
    }
}
```

---

# 🔹 3. Summary (Very Important!)

* **Primitives** → passed as copy → changes don’t affect original.
* **Objects** → reference (address) passed by value → object can be modified.
* **Immutable Objects (String, Wrapper classes)** → new objects created → original stays unchanged.

---



## Wrapper Classes

The wrapper class is a class that wraps (encapsulates) a primitive data type into an object so that it can be used where objects are required.

Need of Wrapper Classes
There are certain needs for using the Wrapper class in Java as mentioned below:

They convert primitive data types into objects. Objects are needed if we wish to modify the arguments passed into a method (because primitive types are passed by value).


The classes in java.util package handle only objects and hence wrapper classes help in this case.


Data structures in the Collection framework, such as ArrayList and Vector, store only objects (reference types) and not primitive types.


An object is needed to support synchronization in multithreading.

Custom Wrapper Classes in Java

Java Wrapper classes wrap the primitive data types. We can create a class that wraps data inside it.


## instance of keyword
The instanceof keyword in Java is used to check whether an object is an instance of a specific class or implements a particular interface. It is a binary operator that returns a boolean value: true if the object is of the specified type, and false otherwise.

Key Points:
It is primarily used for type checking at runtime.

It ensures safe casting by verifying the type before performing a cast.

It works with both classes and interfaces.