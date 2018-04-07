# Errors and Exception Handling

All **Exception Classes** are children of the 'Throwable' class and include a message, stack trace and optional clause.

Exceptions are thrown using the 'throw' keyword or using a try-catch block as follows
```Kotlin
throw ExampleException("Error")

try {
    println("Say something")
} catch(e: ExampleException) {
    println("Something wasn't said")
} finally {
    println("Say another thing")
}
```

*NOTE:* Kotlin down not include checked exceptions like Java, where you throw an exception in the class header.  This leads to broken up code in different places.

'throw' can also be used as part of an elvis expression to signify when the object has no value.
```Kotlin
var test = example.value ?: throw ExampleException("Value is required here")
```
