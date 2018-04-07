# Comparisons of References and Values

Kotlin has two types of equality, Structural Equality and Referential Equality.

**Structural Equality** is checked by the '==' operator similar to calling the .equals() method.  This will return true if both parameter's values are the same.
```Kotlin
var a = 1
val b = 1
if(a==b) println("Both a and b have the same value")
```
**Referential Equality** is checked by the '===' operator.  This will return true if both parameters point to the same object.
```Kotlin
var a = 1
val b = a
if(a===b) println("Both a and b are the same object")
```
