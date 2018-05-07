Does the language have any particularly unique features?

Yes, Kotlin is a statically typed langauge. Some features that are unique to Kotlin are as follows. 

Kotlin is completely compatiable with Java. This is one of the most attractive features of Kotlin because it attracts most Java developers to try it out. 

But, there are some differences between Java and Kotlin that make Kotlin even more unique. These include: 

- Null references are controlled by the type system.
Example: 

```Kotlin
var output: String
output = null   // Compilation error
```

Kotlin protects you from mistakenly operating on nullable types

```Kotlin 
val name: String? = null    // Nullable type
println(name.length())      // Compilation error
```

- No raw types
- Arrays in Kotlin are invariant
- Kotlin has proper function types, as opposed to Java's SAM-conversions
- Use-site variance without wildcards
- Kotlin does not have checked exceptions

Other features include 
- auto casting 

If a type is right, the compiler will auto-cast it for you

```Kotlin
fun calculateTotal(obj: Any) {
    if (obj is Invoice)
        obj.calculateTotal()
}
```

- data classes

As developers, we create classes whose main purpose is to hold data. In such a class some standard functionality and utility functions are often mechanically derivable from the data. In Kotlin, this is called a data class and is marked as data:

```Kotlin
data class User(val name: String, val age: Int)
```