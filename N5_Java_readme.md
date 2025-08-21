# 🚀 Polymorphism in Java

---

## 📖 **Definition**
Polymorphism in Java is one of the **core concepts** in **Object-Oriented Programming (OOP)** that allows objects to behave differently based on their **specific class type**.  

The word **polymorphism** means *having many forms*, and it comes from the Greek words:
- **poly** → many  
- **morph** → forms  

➡ This means **one entity can take many forms**.  
In Java, polymorphism allows the same **method** or **object** to behave differently based on the **context**, especially at **runtime**.

---

## 🔹 **Key Features**
- **Multiple Behaviors** → The same method can behave differently depending on the object calling it.
- **Method Overriding** → A child class can redefine a method of its parent class.
- **Method Overloading** → Multiple methods with the same name but different parameters.
- **Runtime Decision** → At runtime, Java decides which method to call depending on the actual object type.

---

## 💡 **Real-Life Illustration**
Imagine a **Person** who plays different roles:
- 👨 Father  
- 💼 Employee  
- 💍 Husband  

Each role shows **different behavior** based on the context.

---

## 🛠 **Example: Different Roles of a Person**

```java
// Base class Person
class Person {
    void role() {
        System.out.println("I am a person.");
    }
}

// Derived class Father
class Father extends Person {
    @Override
    void role() {
        System.out.println("I am a father.");
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Father();  // Parent reference → Child object
        p.role();                 // Calls Father's overridden method
    }
}
```

# 🔹 Why Use Polymorphism In Java?


### ✅ **1. Code Reusability**
Polymorphism allows the **same method** or **class** to be used with **different types of objects**, making the code **more reusable**.

---

### ✅ **2. Flexibility**
It enables **objects of different classes** to be treated as **objects of a common superclass**, providing flexibility in **method execution** and **object interaction**.

---

### ✅ **3. Abstraction**
Polymorphism allows the use of **abstract classes** or **interfaces**, enabling developers to work with **general types** (like a superclass or interface) instead of concrete types (specific subclasses).  
This **simplifies object interaction**.

---

### ✅ **4. Dynamic Behavior**
With polymorphism, Java can **choose the appropriate method at runtime**, giving the program **dynamic behavior** based on the **actual object type** rather than the **reference type**.

---

## 🛠 **Types of Polymorphism in Java**
In Java, polymorphism is mainly divided into two types:

---

### **1️⃣ Compile-Time Polymorphism (Static)**
- Achieved using **Method Overloading**.
- The method to be executed is decided **at compile time**.

---

### **2️⃣ Runtime Polymorphism (Dynamic)**
- Achieved using **Method Overriding**.
- The method to be executed is decided **at runtime**.
---




# Java Method Overloading Example

## 📌 What is Method Overloading?
**Method Overloading** in Java happens when **two or more methods** in the same class have the **same name** but **different parameter lists**.  
The differences can be:
- **Number of parameters**
- **Type of parameters**
- Or both.

**Note:** The return type alone is **not** enough to distinguish overloaded methods.

---

## 🛠 Example in This Project

We have a `Helper` class with two `Multiply` methods:
1. **`Multiply(int a, int b)`** → Multiplies two integers.
2. **`Multiply(double a, double b)`** → Multiplies two doubles.

---

## 💻 Code

```java
// Helper class with overloaded methods
class Helper {

    // Method with 2 integer parameters
    static int Multiply(int a, int b) {
        return a * b;
    }

    // Method with 2 double parameters
    static double Multiply(double a, double b) {
        return a * b;
    }
}

// Main class to test method overloading
class Geeks {
    public static void main(String[] args) {
        System.out.println(Helper.Multiply(2, 4));       // Calls int version
        System.out.println(Helper.Multiply(5.5, 6.3));  // Calls double version
    }
}

```

