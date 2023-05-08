---
title: "Variables and data types in C#"
datePublished: Mon May 08 2023 00:14:36 GMT+0000 (Coordinated Universal Time)
cuid: clhe3c4no000209mo6mxs9bm0
slug: csharp-variables-and-data-types
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683503903409/fa09a568-892e-4409-965e-440d0016b15d.png
tags: csharp, programming-blogs, programming-languages, data-types, intro-to-programming

---

In C#, there are built-in types (e.g., integers, floating-point numbers, characters, and Booleans) and user-defined (custom) types (e.g., classes, structs, and enums).

Data types specify the kind of data a variable can hold or the kind of values an object can represent. Types are important because they determine the operations that can be performed on the data, the way data is stored in memory, and how it is passed between methods.

A data type defines the kind of values a variable can hold and the operations that can be performed on those values. In other words, a data type is a blueprint, while a variable is a storage location that follows that blueprint.

## Relationship between data types and variables

When we declare a variable, we must specify its data type.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683200468063/81c9a43f-f05e-4d7c-8d6d-a783aa887c3d.png align="left")

This informs the compiler about the kind of data the variable can store and the operations that can be applied to it. In this case, integer values and you can perform operations like addition, subtraction, multiplication, and division on it.

The data type of a variable determines how much memory is allocated for that variable and how the data is interpreted when it's read or modified.

## Data types

In C# and other programming languages, a variable of a **value type** contains an instance of the type. This differs from a variable of a **reference type**, which contains a reference to an instance of the type.

There are **built-in types** included in C# that we can use and serve as the basis for creating more complex **custom types**.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683504047892/891fb268-204d-4294-9be1-ab641a552bf6.png align="center")

1. **Value Type:**
    

* Value types directly contain their data, and memory is allocated on the stack.
    
* When a value type variable is assigned to another variable, a copy of the value is created. Therefore, changes to one variable do not affect the other.
    
* Value types are usually more efficient in terms of memory usage and access speed.
    

1. **Reference Type:**
    

* Reference types store a reference (memory address) to the memory location where the data is stored, rather than the data itself. Memory for reference types is allocated on the heap.
    
* When a reference type variable is assigned to another variable, both variables refer to the same memory location. Therefore, changes made to one variable also affect the other.
    

Here's an example:

```csharp
// *** Value type ***
int a = 10;
int b = a; // We assign the *value* of a to b
b += 5; // We increment the b variable only

Console.WriteLine($"a: {a}, b: {b}"); 
// Output: a: 10, b: 15 

// ***  Reference type ***
// we create a new object of the class StringBuilder
StringBuilder sb1 = new StringBuilder("Hello");
StringBuilder sb2 = sb1; // we assign sb1 to sb2
sb2.Append(", World!"); // we add text to the original string

Console.WriteLine($"sb1: {sb1}, sb2: {sb2}"); 
// Output: sb1: Hello, World!, sb2: Hello, World!
```

In this example, when we assign `a` to `b`, a new copy of the value is created. Thus, modifying `b` does not affect `a`. However, when we assign `sb1` to `sb2`, both variables reference the same memory location, so changes made to one variable are visible to the other.

## Summary of Data types

Here's a summary of the different kind of value types and reference types available in C#.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683504092940/eb19f7ef-1f5c-422b-ab27-430a19638949.png align="center")

## Conclusion

In conclusion, C# offers various data types that help manage how data is stored, accessed, and manipulated. Understanding the differences between value types and reference types, as well as built-in and custom types, is essential for efficient programming in C#.

## Reference

* [.NET class library overview | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/standard/class-library-overview)
    
* [The C# type system | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/)
    
* [Integral numeric types - C# reference | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types)
    
* [Floating-point numeric types - C# reference | Microsoft Learn](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/floating-point-numeric-types)