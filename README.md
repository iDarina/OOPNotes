## Java Class Essentials

### Class Basics
- A **class** is a template for creating objects.
- Declared with the `class` keyword followed by the class name.
- The body of the class is contained within curly braces `{}`.
- Java source file names normally match the class name.

### Object
- An **object** is an instance of a class.
- The object is created using the `new` keyword.
- **Classes are reference types** – class variables hold a reference to an object.
- Multiple variables can reference the same instance.

---

### Class Structure
Classes contain:

- **Fields**: 
  - Store the object's state.
  
- **Methods**:
  - Contain executable code.
  - Manipulate the state and perform operations.
  
- **Constructors**:
  - Executable code that runs during object creation.
  - Sets the initial state of the object.

---

### Special References
- **`this`**: Implicit reference to the current object.
- **`null`**: Represents an uncreated object or a null reference.

---

### Access Modifiers
- Control the visibility of a class and its members (fields, methods).
- Enable **encapsulation** in Java.

### Accessing Fields
- Fields are not normally directly accessible.
  - **Accessors** (getters) retrieve field values.
  - **Mutators** (setters) modify field values.

---

### Class Instances and Initial State
- Every new instance of a class is initialized with a default state.
  - **Numeric fields**: Initialized to `0`.
  - **Reference fields**: Initialized to `null`.

### Field Initializers
- Assign specific values to fields when they are declared, known as **field initializers**.
- These can be simple assignments or involve equations, other fields, or method calls.

### Constructors
- Constructors allow code execution during object creation and can accept parameters.
- A **default constructor** accepts no parameters.
- A class can have multiple constructors, and the one used depends on the parameters passed.
- One constructor can call another, but this call must be the first line, passing data between constructors.

### Nonpublic Constructors
- Constructors can be nonpublic, restricting object creation from outside the class.

### Initialization Blocks
- **Initialization blocks** run during object creation and are independent of specific constructors.
- They cannot receive parameters and execute regardless of which constructor is used.


## Key Points on Static Members in Java

### 1. Static Members Overview
- **Static members** are class-wide, shared across all instances of a class.
- Indicated by the `static` keyword in their declaration.

### 2. Static Fields
- A **static field** is not associated with any specific instance of the class.
- All instances of the class access the **same** static field value.

### 3. Static Methods
- **Static methods** perform actions not tied to an instance but to the class itself.
- Static methods can only access **static fields** and **other static methods**.

### 4. Static Import
- The **static import** statement provides a shorthand for accessing static methods.
- Allows you to use static methods without prefixing them with their class name.

### 5. Static Initialization Blocks
- **Static initialization blocks** allow for one-time type initialization.
- The code inside these blocks runs **before** the type’s first use, making them ideal for setup tasks.


