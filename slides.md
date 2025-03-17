---
theme: excali-slide
background: https://cover.sli.dev
title: Names, Bindings, and Scopes
info: |
  ## Slidev Starter Template
  Presentation slides for developers.
  Learn more at [Sli.dev](https://sli.dev)
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Names, Bindings, and Scopes

**Presentation of GROUP 2**

---
transition: slide-left
---

## Names

A name is a string of characters used to identify some entity in a program.
Names in programming languages have the same form: starting with a letter
followed by a string consisting of letters, digits, and underscore (_)
characters. The term “identifier” can be used interchangeably with “name”.

The use of underscore to form names was used in the 1970s-1980s but is now far
less popular. In the C-based languages, it has been replaced by camel notation
or camel case, in which all of the words of a multiple-word name except the
first are capitalized, as in `myFirstCode`. It is called “camel” as words
written as names often have embedded uppercase letters, making it look like a
camel’s hump.

---

## Common Naming Conventions

| Name       | Description                                               | Example            |
| ---------- | --------------------------------------------------------- | ------------------ |
| Kebab-case | Words are lowercase and separated by hyphens              | `my-variable-name` |
| Snake_case | Words are lowercase and separated by underscores          | `my_variable_name` |
| CamelCase  | Each word is capitalized without spaces                   | `MyVariableName`   |
| camelCase  | First word is lowercase, subsequent words are capitalized | `myVariableName`   |
| PascalCase | Similar to CamelCase, but often used for class names      | `MyClassName`      |

---

## Naming convention based on popular programming languages

| Language   | Convention                                                      | Example                   |
| ---------- | --------------------------------------------------------------- | ------------------------- |
| Python     | Snake case for variables and functions, Pascal case for classes | `my_variable`, `MyClass`  |
| Java       | Camel case for variables and methods, Pascal case for classes   | `myVariable`, `MyClass`   |
| C#         | Camel case for variables and methods, Pascal case for classes   | `myVariable`, `MyClass`   |
| JavaScript | Camel case for variables and functions, Pascal case for classes | `myVariable`, `MyClass`   |
| Rust       | Snake case for variables and functions, Pascal case for types   | `my_variable`, `MyType`   |
| PHP        | Snake case for variables and functions, Pascal case for classes | `$my_variable`, `MyClass` |

---

## Special Words

These are used to make programs more readable by naming actions to be performed.
They separate the syntactic parts of statements and programs. In most languages,
these are known as reserved words that cannot be redefined by programmers. But
in some cases, such as Fortran, they are only keywords wherein they can be
redefined.

A reserved word is a special word that cannot be used as a name in a programming
language. This becomes difficult and a problem for programmers if the language
includes many reserved words. For example, COBOL has 300 reserved words wherein
some of the most commonly chosen names are in the list of reserved words such as
LENGTH, BOTTOM, DESTINATION, and COUNT. Most times, a programming environment
would assign specific text colors to reserved words once used.

---

## Special Words

Here are the identifiers used as reserved words in Python.

| Reserved Word | Description                                       | Example                 |
| ------------- | ------------------------------------------------- | ----------------------- |
| `False`       | Represents the boolean value false                | `a = False`             |
| `None`        | Represents the absence of a value or a null value | `a = None`              |
| `True`        | Represents the boolean value true                 | `a = True`              |
| `and`         | Logical AND operator                              | `a and b`               |
| `as`          | Used to create an alias                           | `import math as m`      |
| `assert`      | For debugging purposes                            | `assert a == b`         |
| `async`       | Declares an asynchronous function                 | `async def foo(): pass` |

---

## Special Words

| Reserved Word | Description                               | Example               |
| ------------- | ----------------------------------------- | --------------------- |
| `await`       | Waits for the result of an async function | `await foo()`         |
| `break`       | Terminates a loop                         | `break`               |
| `class`       | Declares a class                          | `class MyClass: pass` |
| `continue`    | Skips the rest of the loop iteration      | `continue`            |
| `def`         | Declares a function                       | `def my_func(): pass` |
| `del`         | Deletes an object                         | `del a`               |
| `elif`        | Else if condition                         | `elif a == b:`        |
| `else`        | Else condition                            | `else:`               |

---

## Special Words

| Reserved Word | Description                                | Example               |
| ------------- | ------------------------------------------ | --------------------- |
| `except`      | Handles exceptions                         | `except ValueError:`  |
| `finally`     | Executes code regardless of exceptions     | `finally:`            |
| `for`         | For loop                                   | `for i in range(5):`  |
| `from`        | Imports specific parts of a module         | `from math import pi` |
| `global`      | Declares a global variable                 | `global a`            |
| `if`          | If condition                               | `if a == b:`          |
| `import`      | Imports a module                           | `import math`         |
| `in`          | Checks if a value is present in a sequence | `if a in b:`          |

---

## Special Words

| Reserved Word | Description                   | Example                     |
| ------------- | ----------------------------- | --------------------------- |
| `is`          | Tests object identity         | `if a is b:`                |
| `lambda`      | Creates an anonymous function | `lambda x: x + 1`           |
| `nonlocal`    | Declares a non-local variable | `nonlocal a`                |
| `not`         | Logical NOT operator          | `not a`                     |
| `or`          | Logical OR operator           | `a or b`                    |
| `pass`        | Null statement, does nothing  | `pass`                      |
| `raise`       | Raises an exception           | `raise ValueError("error")` |

---
transition: slide-up
---

## Variables

A variable in programming is an abstraction of a computer memory cell or
collection of cells. It can be characterized as a sextuple of attributes
including name, address, type, value, lifetime, and scope.

- **Variable Names** – the most common names in programs. These are used to
  identify and reference values that can change. They can be made up of letters,
  numbers, and underscores and should be descriptive and meaningful.

```python
age = 25
name = "Alice"
is_student = True
```

---
transition: slide-up
---

## Variables

**Variable Address** – the address of a variable is the unique machine memory
address it is associated with. It acts as a numerical identifier that allows the
program to access and manipulate the data held by the variable.

```python
import ctypes

x = 10
address = id(x)
print(f"The address of variable x is: {address}")
```

---
transition: slide-up
---

## Variables

**Variable Type** – determines the range of values the variable can store and
the set of operations defined for values of the type. Examples include int,
float, and Boolean.

```python
integer_var = 10
float_var = 10.5
boolean_var = True
print(type(integer_var))  # <class 'int'>
print(type(float_var))    # <class 'float'>
print(type(boolean_var))  # <class 'bool'>
```

---
transition: slide-up
---

## Variables

**Variable Value** – the contents of the memory cell or cells associated with
the variable. A variable’s value can also be called its r-value, as it is
required when the variable name appears on the right side of an assignment
statement.

```python
x = 5
print(f"The value of x is: {x}")
```

---
transition: slide-up
---

## Variables

**Variable Lifetime** – the amount of time it exists and retains its value in
memory, depending on how and where it is declared.

```python
def my_function():
  y = 10  # y is created when the function is called
  print(y)
my_function()
# y no longer exists after the function call
```

---
transition: slide-up
---

## Variables

**Variable Scope** – the part of the program where a variable can be accessed.
It is determined by where the variable is declared in the code.

```python
z = 20  # Global scope

def my_function():
  a = 30  # Local scope
  print(a)
  print(z)  # Accessing global variable

my_function()
print(z)  # Accessing global variable
# print(a)  # This would raise an error because 'a' is not in the global scope
```

---
layout: center
---

## Bindings

---

## Bindings

**Binding** is an association between an attribute and an entity, such as
between a variable and its type or value, or between an operation and a symbol.
Binding time is the time a binding takes place, for instance, at language design
time, language implementation time, compile time, load time, link time, or run
time.

For example, the asterisk (*) symbol is often bound to the multiplication
operation at language design time. A data type, such as int, is bound to a range
of possible values at language implementation time. A variable in a Java program
is bound to a particular data type at compile time.

---

## Bindings

Using this assignment statement:

```python
count = count - 3
```

The variable `count` is bound to its value at run time.

- The type of count is bound at compile time
- The set of possible values of count is bound at compiler design time
- The meaning of the operator symbol – is bound at compile time, when the types
  of its operands have been determined
- The internal representation of the literal 3 is bound at compiler design time
- The value of the count is bound at execution time with this statement

---

# Dynamic Programming

In dynamic programming languages like Python, variables are not bound to a
specific type and can change types at runtime.

```python
# Dynamic typing in Python
x = 10          # x is an integer
print(type(x))  # <class 'int'>

x = "Hello"     # x is now a string
print(type(x))  # <class 'str'>

x = [1, 2, 3]   # x is now a list
print(type(x))  # <class 'list'>
```

---

# Static Programming

In static programming languages like Rust, variables are bound to a specific
type at compile time and cannot change types.

```rust
// Static typing in Rust
fn main() {
  let x: i32 = 10;  // x is an integer
  println!("{}", x);
  // x = "Hello";  // This would cause a compile-time error
}
```

---
layout: center
---

## Type Bindings

---

## Type Bindings

**Type Bindings** A variable must be bound to a data type before being
referenced in a program. Aside from the binding time, it is also important to
know how the type is specified. Types can be defined statically by some form of
_**explicit**_ or _**implicit**_ declaration.

An **explicit** declaration is a statement in a program that lists variable
names and specifies their particular type. It directly specifies the data type
of the variable when declaring it.

For example, in C:

```c
int number; // Explicitly declares 'number' as an integer [1, 2, 5]
float decimal; // Explicitly declares 'decimal' as a floating-point number [1.3, 2.5]
char letter; // Explicitly declares 'letter' as a character [A, B, C]
```

---

## Type Binding

In older programming languages, variables can often be explicitly declared with
a specific type, but they can also be nullable. This means that a variable can
hold a value of the declared type or a special null value indicating the absence
of a value.

Here's an example in Java:

```java
String name; // Declared as a String type but not initialized
name = null; // Explicitly set to null
```

---

## Type Binding - Why is this dangerous?

1. **Undefined Behavior**: If you try to use a variable that is null without
   checking, it can lead to undefined behavior or crashes. For example, calling
   a method on a null object will result in a `NullPointerException` in Java.

   ```java
   String name = null;
   int length = name.length(); // This will throw a NullPointerException
   ```

2. **Hard to Debug**: Null-related bugs can be difficult to track down because
   the null value can propagate through the code, causing errors far from the
   original source.

3. **Inconsistent State**: Allowing null values can lead to inconsistent states
   within the application, making it harder to reason about the code.

---

## Type Binding - Modern Approaches

Modern languages and frameworks often provide ways to avoid these issues:

- **Non-nullable Types**: Some languages, like Kotlin, have non-nullable types
  by default. You have to explicitly declare if a variable can be null.

  ```kotlin
  var name: String = "John" // Non-nullable
  var nullableName: String? = null // Nullable
  ```

- **Optional Types**: Languages like Swift and TypeScript use optional types to
  handle nullability more safely.

  ```typescript
  let name: string | null = null; // TypeScript
  ```

By using these modern approaches, you can reduce the risk of null-related errors
and make your code more robust and maintainable.

---

## Type Bindings

An implicit declaration is a means of associating variables with types through
default conventions rather than declaration statements. It automatically assigns
the variable’s data type based on its usage within the code without an explicit
declaration statement. Both declarations create static bindings to types.

---

## Rust

In **Rust**, variables are usually explicitly declared, but type inference can
be used to implicitly determine the type based on the assigned value.

```rust
fn main() {
  let x = 42; // Implicitly inferred as i32
  println!("x is {}", x);
}
```

---

## Go

In Go, the `:=` operator can be used for implicit declaration and type
inference.

```go
package main

import "fmt"

func main() {
  x := 42 // Implicitly inferred as int
  fmt.Println(x)
}
```

---

## Python

In Python, variables are dynamically typed, and their types are implicitly
determined based on the assigned value.

```python
x = 42  # Implicitly inferred as int
print(f"x is {x} and its type is {type(x)}")
```

---

In Python, variables are dynamically typed, so it is unnecessary to declare
their types explicitly. However, the concept of explicit declaration can still
be applied by binding a variable to a value and showing that the variable can
later change its type.

For example, a program to demonstrate explicit declaration and binding:

```python
# Explicit variable declaration and binding
# Binding an integer to variable 'x'
x = 10
print(f"x is bound to {x} and its type is {type(x)}")
# Now, binding a string to the same variable 'x'
x = "Hello, world!"
print(f"x is now bound to '{x}' and its type is {type(x)}")
# Binding a float to 'x'
x = 3.14
print(f"x is now bound to {x} and its type is {type(x)}")
# Binding a list to 'x'
x = [1, 2, 3]
print(f"x is now bound to {x} and its type is {type(x)}")
```

---

## Type Binding

The previous Python example demonstrates explicit variable declaration and
binding, but it can be misleading due to the dynamic nature of Python's type
system. In Python, variables are not bound to a specific type, and their type
can change at runtime. This flexibility can lead to complexity and confusion
about what the variables really do.

Here's a breakdown of how the type system works in Python and how it can be
overridden:

---

## Python's Dynamic Typing

In Python, variables are dynamically typed, meaning that the type of a variable
is determined at runtime. You can assign any type of value to a variable, and
you can change the type of the variable by assigning a new value of a different
type.

### Example of Dynamic Typing

```python
# Initial binding of an integer to variable 'x'
x = 10
print(f"x is bound to {x} and its type is {type(x)}")

# Rebinding 'x' to a string
x = "Hello, world!"
print(f"x is now bound to '{x}' and its type is {type(x)}")

# Rebinding 'x' to a float
x = 3.14
print(f"x is now bound to {x} and its type is {type(x)}")

# Rebinding 'x' to a list
x = [1, 2, 3]
print(f"x is now bound to {x} and its type is {type(x)}")
```

---

## Potential Issues

1. **Type Confusion**: Since the type of a variable can change, it can be
   difficult to track what type a variable holds at any given point in the code.
   This can lead to bugs and unexpected behavior.

2. **Readability**: Code readability can suffer because the type of a variable
   is not explicitly declared and can change, making it harder for other
   developers (or even the original developer) to understand the code.

3. **Runtime Errors**: Type-related errors will only be caught at runtime, which
   can make debugging more challenging.

---

## Example of Type Confusion

```python
x = 10  # x is an integer
x = "Hello"  # x is now a string
x = x + 5  # This will raise a TypeError because you cannot add an integer to a string
```

### Best Practices

To mitigate these issues, consider the following best practices:

1. **Type Annotations**: Use type annotations to indicate the expected type of a
   variable. This can improve code readability and help with static type
   checking tools like `mypy`.

```python
x: int = 10
x = "Hello"  # This will raise a type checker warning
```

2. **Consistent Typing**: Try to keep the type of a variable consistent
   throughout its scope to avoid confusion.

3. **Descriptive Variable Names**: Use descriptive variable names that indicate
   the type or purpose of the variable.

---

## Scopes

The scope of a variable is the range of statements wherein the variable is
visible. A variable is visible in a statement if it can be referenced or
assigned in that statement.

Furthermore, scope refers to the region of a program where a particular variable
or function is accessible and valid. It determines the lifetime and visibility
of a variable, meaning where it can be used and modified within the code.

---

## Types of Scope - Global Scope:

**Global Scope**: Variables declared in the global scope are accessible from
anywhere in the program, including inside functions or methods. They are usually
defined outside of any function or block of code.

Example in Python:

```python
x = 10  # Global variable
def my_function():
  print(x)  # x is accessible here because it is in global scope
my_function()  # This will print 10
```

Example in JavaScript:

```javascript
var x = 10; // Global variable
function myFunction() {
  console.log(x); // x is accessible here because it is in global scope
}
myFunction(); // This will print 10
```

---

## Types of Scope - Global Scope:

Example in C#:

```csharp
using System;

class Program
{
    static int x = 10;  // Global variable
    static void MyFunction()
    {
        Console.WriteLine(x);  // x is accessible here because it is in global scope
    }
    static void Main()
    {
        MyFunction();  // This will print 10
    }
}
```

---

## Types of Scope - Local Scope:

**Local Scope**: Variables declared inside a function or block of code are local
variables and can only be accessed within that specific function or block. They
are not visible outside their defining scope.

Example in Python:

```python
def my_function():
  y = 5  # Local variable
  print(y)
my_function()  # This will print 5
print(y)  # This will raise an error because 'y' is not accessible outside the function
```

Example in JavaScript:

```javascript
function myFunction() {
  let y = 5; // Local variable
  console.log(y);
}
myFunction(); // This will print 5
console.log(y); // This will raise an error because 'y' is not accessible outside the function
```

---

## Types of Scope - Local Scope:

Example in C#:

```csharp
using System;

class Program
{
    static void MyFunction()
    {
        int y = 5;  // Local variable
        Console.WriteLine(y);
    }
    static void Main()
    {
        MyFunction();  // This will print 5
        // Console.WriteLine(y);  // This will raise an error because 'y' is not accessible outside the function
    }
}
```

---

## Types of Scope - Enclosing Scope:

**Enclosing Scope**: This refers to the scope of a function that encloses
another function. If there is a nested function, the outer function's variables
are available to the inner function, but not the other way around.

Example in Python:

```python
def outer_function():
  z = 15  # Enclosing variable
  def inner_function():
    print(z)  # Accessing the enclosing scope variable
  inner_function()  # This will print 15
outer_function()
```

Example in JavaScript:

```javascript
function outerFunction() {
  let z = 15; // Enclosing variable
  function innerFunction() {
    console.log(z); // Accessing the enclosing scope variable
  }
  innerFunction(); // This will print 15
}
outerFunction();
```

---

## Types of Scope - Enclosing Scope:

Example in C#:

```csharp
using System;

class Program
{
    static void OuterFunction()
    {
        int z = 15;  // Enclosing variable
        void InnerFunction()
        {
            Console.WriteLine(z);  // Accessing the enclosing scope variable
        }
        InnerFunction();  // This will print 15
    }

    static void Main()
    {
        OuterFunction();
    }
}
```

---

## Types of Scope - Built-in Scope:

**Built-in Scope**: The built-in scope contains all the functions and variables
that are built into Python, like print(), len(), and int(). These are always
available to use.

Example in Python:

```python
print(len([1, 2, 3])) # Using built-in function `len`
```

Example in JavaScript:

```javascript
console.log([1, 2, 3].length); // Using built-in property `length`
```

---

## Scope Rules

Here are some scope rules in Python and many other languages

LEGB Rule: Python follows the LEGB rule when looking up variables, which stands
for:

- Local (innermost scope)
- Enclosing (any enclosing functions, like in closures)
- Global (the module-level scope)
- Built-in (the scope that contains Python’s built-in objects and functions)

Shadowing: If a variable declared in a local scope has the same name as a
variable in an outer (enclosing or global) scope, it shadows the outer variable,
meaning the local variable takes precedence. For example,

```python
x = 100 # Global variable
def my_function():
  x = 50 # Local variable, shadows the global variable
  print(x)
my_function() # Prints 50, because the local x shadows the global x
print(x) # Prints 100, the global x remains unchanged
```

---

## Scope Rules

Example in Rust:

```rust
fn main() {
    let x = 100; // Global variable

    {
        let x = 50; // Local variable, shadows the global variable
        println!("{}", x); // Prints 50, because the local x shadows the global x
    }
    
    println!("{}", x); // Prints 100, the global x remains unchanged
}
```

---

`global` Keyword: In Python, to modify a global variable inside a function, it
must be declared with a global keyword to avoid creating a local variable with
the same name.

For example:

```python
x = 10
def modify_global():
  global x # Declare that we are modifying the global variable 'x'
  x = 20
modify_global()
print(x) # Prints 20
```

---
layout: center
---

## The end

---
