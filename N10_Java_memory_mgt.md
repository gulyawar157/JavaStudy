### Instance Variables in Java
1. What are they?
- Instance variables are variables declared inside a class but outside any method, constructor, or block.
- They belong to an object (instance) of the class.
- Each object gets its own copy of instance variables.

### Key Features
- Declared inside class, but outside methods.
- Stored in the Heap (inside the object).
- Default values are automatically given (e.g., 0 for int, null for objects, false for boolean).
- Each object has its own copy.

```java
class Student {
    // Instance variables
    String name;
    int age;

    void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();
        s1.name = "Aman";
        s1.age = 20;

        Student s2 = new Student();
        s2.name = "Neha";
        s2.age = 22;

        s1.display();  // Name: Aman, Age: 20
        s2.display();  // Name: Neha, Age: 22
    }
}
```

- In short:
Instance variables are the variables tied to an object of a class. Each object has its own copy, and they live as long as the object lives.



## Stack and Heap

### Stack (Method Stack)
- What is it?
Special memory area that stores method calls and local variables.

How it works:

- Every time a method is called → a new stack frame is created.
- The frame contains method parameters + local variables + return address.
- When method finishes → its frame is removed (popped).

Key Points:
- Stores primitive values (int, char, float, …).
- Stores references (addresses) to objects (but the objects themselves live in the heap).
- Fast access, small memory, automatically cleared when method ends.

### Heap
- What is it?
A large pool of memory used to store objects and instance variables.

How it works:

- Whenever you use new in Java, the object is created in the heap.
- Even if method ends, object stays in heap until garbage collector removes it.

Key Points:
- Stores objects and their instance variables.
- Shared across all threads.
- Managed by Garbage Collector (GC).

3. Stack ↔ Heap Relationship

Stack holds reference variables.
Heap holds the actual objects.




| **Type**              | **Where Declared**                  | **Lifetime**             | **Shared?**                    |
| --------------------- | ----------------------------------- | ------------------------ | ------------------------------ |
| **Instance Variable** | Inside class, outside methods       | As long as object exists | No (per object)                |
| **Local Variable**    | Inside method/constructor/block     | Until method ends        | No                             |
| **Static Variable**   | Inside class, with `static` keyword | Entire program           | Yes (one copy for all objects) |



 Summary Table
Feature	Stack	Heap
Stores	Method calls, local vars, refs	Objects & instance variables
Lifetime	Cleared when method ends	Until GC deletes object
Access speed	Very fast	Slower
Size	Small	Large
Managed by	JVM automatically (push/pop)	Garbage Collector

✅ In short:

Stack → short-lived, stores method calls & local variables.

Heap → long-lived, stores objects created with new.