# IOS Development

> A quick guide through Swift and IOS programming concepts.

## Swift ![Swift](./appDev/swift.png)

### What is it?

Swift is a **general-purpose**, **multi-paradigm**, compiled programming language developed by Apple Inc.
Swift was developed as a replacement for Apple's earlier programming language Objective-C.

## Syntax and Semantics

- **Syntax** - Determines if a program is well formed.
- **Semantics** - Refers to the meaning of a statement.

A **statement** is a command to perform an action.
In swift we do not need to end a statement with a semi-colon => `;`.

Commenting in Swift:

- `//` => One line comment
- `/* code block */` => Block comments

### Syntax

Let's assume a class called `MyClass`.  
In Swift we name the file the same as the class.

**Keywords**  
This are words reserved with a specific meaning to the compiler and cannot be used for other purposes.

![[Keywords](https://docs.swift.org/swift-book/ReferenceManual/LexicalStructure.html)](./appDev/keywords.JPG)

---

## Data Types

Swift is a strongly typed language, meaning that all data consists of a **value** and a **type**.

### Types of Data

- int
- float
- double
- bool
- string
  - Strings in swift are unicode
- char
- optional
- tuples
  - `(code: Int, message : String)`
  - `(s1,s2) = (s2,s1) => //s1 becomes s2 and s2 becomes s1`

#### Variables

A variable refers to a memory location whose contents can be changed during program execution.

All variables must have the following characteristics:

- **Identifier**
- **Value**

Swift has type inference meaning you can either put the type of the variable or not, the compiler will do it for you in case you don't put it. (Only on default values)

##### Identifiers

In swift we have two types of data, **Constants** and **Variables**.

- **`let`** identifier is used for constants.
- **`var`** identifier is used for variables.

We declare variables the following way: **`identifier variableName`**

Examples:

- `let number = 18`
- `var name = "joao"`
- `var name: String`

---

### Functions

Functions are named code blocks. Functions can have arguments and return values and correspond to **procedures** or **methods** in other languages.

```swift
// Declaring a function
func methodName(parameters: Type) -> ReturnType {
    ...
}
```

- **ReturnType** is the type of the value returned.
- **MethodName** an identifier.
- **parameters** a list of arguments, each with an identifier.

Example:

```swift
func sum(a: Int, b: Int){
    return a + b;
}
```
