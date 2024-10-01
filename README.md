
  # Video-Lecture
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


# Head-First Book
- Objects are born and objects die.
- You decide when and how to **construct** it.
- You decide when to **destroy** it.
- **Garbage Collector** can vaporize it, reclaiming the memory that object was using.

### The Stack and the Heap: where things live
- All ***objects*** live on the garbage-collectible heap.
- Loval variables are also known as ***stack*** variables.

### Instance Variables
- Instance variables are declared inside a ***class*** but not inside a method.

### Local Variables
- Local variables are declared inside a ***method***, including method parameters.


- Java has two areas of memory we care about: the Stack and the Heap.
- Instance variables are variables declared inside a class but outside any method.
- Local variables are variables declared inside a method or method parameter.
- All local variables live on the stack, in the frame corresponding to the method where the variables are declared.
- Object reference variables work just like primitive variables - if the reference is declared as a loval variable, it goes on the stack.
- All objects live in the heap, regardless of whether the reference is a local or instance variable.
- Instance variables live within the object they belong to, on the Heap.
- If the instance variable is a reference to an object, both the reference and the object it referc to are on the Heap.
- A constructor is the code that runs when you say `new` on a class type.
- A constructor must have the same name as the class, and must ***not*** have a return type.
- You can use a constructor to initialize the state (i.e. the instance variables) of the object being constructed.
- If you don't put a constuctor in your class, the compiler will put in a default constructor.
- The default constructor is always a no-arg constructor.
- If you put a constructor - any constructor - in your class, the compiler will not build the default constructor.
- If you want a no-arg constructor, and you've already put in a constructor with arguments, you'll have to build the no-arg constructor yourself.
- Always provide a no-arg constructor if you can, to make it easy for programmers to make a working object. Supply default values.
- Overloaded constructors means you have more than one constructor in your class.
- Overloaded constructors must have different argument lists.
- You cannot have two constructors with the same argument lists. An argument list includes the order and/or type of arguments.
- Instance variables are assigned a default value, even when you don't explicity assign one. The default values are 0/0.0/false for primitives, and null for references.
