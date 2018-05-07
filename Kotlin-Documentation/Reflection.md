What reflection abilities are supported?
How is reflection used?

Reflection is a set of language and library features that allows for introspecting the structure of your own program at runtime. Kotlin makes functions and properties first-class citizens in the language, and introspecting them (i.e. learning a name or a type of a property or function at runtime) is closely intertwined with simply using a functional or reactive style.

References to functions, properties, and constructors, apart from introspecting the program structure, can also be called or used as instances of function types.

In short you can do:
1. Class References 
2. Bound Class References 
3. Callable references 
4. Function references 
5. Property references 
6. Interoperability with Java Reflection
7. Constructor references

The most basic reflection feature is getting the runtime reference to a Kotlin class. To obtain the reference to a statically known Kotlin class, you can use the class literal syntax:

```Kotlin 
val c = MyClass::class```

The reference is a value of type KClass.

