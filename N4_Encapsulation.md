Encapsulation in Java
Last Updated : 06 Aug, 2025
In Java, encapsulation is one of the core concepts of Object Oriented Programming (OOP) in which we bind the data members and methods into a single unit. Encapsulation is used to hide the implementation part and show the functionality for better readability and usability. The following are important points about encapsulation.

Better Code Management: We can change data representation and implementation any time without changing the other codes using it if we keep method parameters and return values the same. With encapsulation, we ensure that no other code would have access to implementation details and data members.
Simpler Parameter Passing: When we pass an object to a method, everything (associated data members and methods are passed along). We do not have to pass individual members.
getter and setter: getter (display the data) and setter method ( modify the data) are used to provide the functionality to access and modify the data, and the implementation of this method is hidden from the user. The user can use this method, but cannot access the data directly.
Example: Below is a simple example of Encapsulation in Java.




// Java program demonstrating Encapsulation
class Programmer {
    
    private String name;
​
    // Getter and Setter for name
    
    // Getter method used to get the data
    public String getName() { return name; }
    
    // Setter method is used to set or modify the data
    public void setName(String name) { this.name = name; }
}
​
public class Geeks {
    
    public static void main(String[] args) {
        Programmer p = new Programmer();
        p.setName("Geek"); 
        System.out.println("Name=> " + p.getName());
    }
}

Output
Name=> Geek
Explanation: In the above example, we use the encapsulation and use getter (getName) and setter (setName) method which are used to show and modify the private data. This encapsulation mechanism protects the internal state of the Programmer object and allows for better control and flexibility in how the name attribute is accessed and modified.

Uses of Encapsulation in Java
Using encapsulation in Java has many benefits:

Data Hiding: The internal data of an object is hidden from the outside world, preventing direct access.
Data Integrity: Only validated or safe values can be assigned to an object’s attributes via setter methods.
Reusability: Encapsulated code is more flexible and reusable for future modifications or requirements.
Security: Sensitive data is protected as it cannot be accessed directly.
This image below demonstrates the concept of encapsulation, where a class (represented by the capsule) hides its internal data (variables) and only exposes a controlled interface (encapsulation).

encapsulation
Encapsulation
Implementation of Java Encapsulation
In Java, encapsulation is implemented by declaring instance variables as private, restricting direct access. Public getter methods retrieve variable values, while setter methods modify them, enabling controlled access. This approach allows the class to enforce data validation and maintain a consistent internal state, enhancing security and flexibility.

Encapsulation is defined as the wrapping up of data under a single unit. It is the mechanism that binds together code and the data it manipulates. Another way to think about encapsulation is, that it is a protective shield that prevents the data from being accessed by the code outside this shield. 

In encapsulation, the variables or data of a class are hidden from any other class and can be accessed only through any member function of its own class.
A private class can hide its members or methods from the end user, using abstraction to hide implementation details, by combining data hiding and abstraction.
Encapsulation can be achieved by Declaring all the variables in the class as private and writing public methods in the class to set and get the values of variables.
It is more defined with the setter and getter method.