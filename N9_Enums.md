### What is enum in Java?
- enum (short for enumeration) is a special data type in Java.
- It is used to define a set of fixed constants (values that don’t change).
Example: Days of the week, Months, Directions, Order Status, etc.

👉 enum makes your code more readable and type-safe (instead of using raw integers or strings).


🔹 1. What is a POJO?

POJO = Plain Old Java Object.

It’s just a simple Java class with fields, constructors, getters, setters, and maybe toString(), equals(), hashCode().

It does not depend on any framework or library.

Example:

```java

public class User {
    private String name;
    private int age;

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Getters & Setters
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
    public int getAge() { return age; }
    public void setAge(int age) { this.age = age; }

    @Override
    public String toString() {
        return name + " (" + age + ")";
    }
}

```
This is a POJO because it’s just a plain Java object.

🔹 2. What is a Model Class?
A Model class is also usually a POJO, but it is specifically used to represent data in an application.

In MVC architecture (Model-View-Controller):

Model = represents the data (and sometimes business logic).

View = UI (what the user sees).

Controller = handles requests and responses.

👉 So, a Model class is basically a POJO that represents real-world data (like User, Product, Employee, etc.), often mapped to a database table if you’re using frameworks like Hibernate/JPA.

🔹 3. Difference between POJO and Model Class
Aspect	POJO	Model Class
Meaning	Just a plain Java object	A POJO that represents application data (in MVC, DB, APIs, etc.)
Usage	Can be used anywhere	Used specifically for data representation in apps
Example	User, Address, Book	UserModel, ProductModel, EmployeeModel (represent DB rows or API payloads)
Relationship	Every model class is a POJO	But not every POJO is necessarily a model

✅ So:

A POJO = concept (simple object).

A Model class = role (POJO used to represent data in MVC or DB).

👉 Example:

```java

// POJO
public class Product {
    private int id;
    private String name;
    private double price;
    
    // constructors, getters, setters...
}

// Model (POJO playing the role of "data model")
public class ProductModel extends Product {
    // Maybe extra methods or DB annotations
    // Example: @Entity for Hibernate
}

```
⚡ In practice:
If you’re learning, just remember 👉 a Model class is a POJO used to represent real-world data in your app.