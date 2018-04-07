# Types
In Kotlin, all types behave like objects, no primitive typing.

(Variables only stored as reference, not value)

New classes to hold objects can be made, but new value types cannot be created.

In Kotlin variables and values do not have to have the type specified, they *can* specify, but it is not required.  This is shown below
```Kotlin
var x = 1       // new variable x of implied type Int
val y: Int = 2  // new value y of explicit type Int
```

## Basic types

**Numbers** are represented as objects, similar to Java where you have:
* Double
* Float
* Long
* Int
* Short
* Byte

```Kotlin
var double: Double = 1234567
var float: Float = 2.2
var long: Long = 4.4444
var int: Int = 9
var short: Short = 1
var byte: Byte = 0
```

**Explicit Conversion** between number types happen by calling the following functions on the object, these functions are available for all number types
* toByte()
* toShort()
* toLong()
* toInt()
* toFloat()
* toDouble()
* toChar()

```Kotlin
var x: Long = 1
var y: Int = x.toInt()
```
**Characters** are represented by the object 'Char' and go in single tick quotes.
```Kotlin
val example: Char = 'X'
```
Escape characters are also supported as follows: \t, \b, \n, \r, \', \", \\, \$

**Strings** are represented by the immutable object 'String'.
Strings can be accessed like character arrays with array notation, as well as iterated with a for-loop.
```Kotlin
var full: String = "Hello"
var first: Char = full[0]
```

Strings are concatenated with the '+' operator
```Kotlin
var one: String = "Abra Kadabra"
var two = "Alakazam"
var result = one + " " + two  // "Abra Kadabra Alakazam"
```

Raw strings are also supported and denoted by 3 double-ticks before and after.  Raw strings can contain characters that would normally escape the string like new lines.
```Kotlin
var text: String = """
    This is a lot of text.
    You can place characters like "this" that would normally escape.
"""
```

String Templates are denoted with a '$' inside of the string, expressions that need to be evaluated are surrounded with'{}' after the '$'
```Kotlin
var pi = 3.14
println("The number Pi is $x")
println("Pi as an int is ${x.toInt()}")
```

**Booleans** are represented by the object 'Boolean' and can be either *true* or *false*

Booleans can also be compared using the following operators
* || - OR
* && - AND
* !  - NOT

```Kotlin
var t1: Boolean = true
var t2 = true
var t3 = t1 && t2   // Evaluates to true
```

**Arrays** are represented by the object 'Array', they can be created a number of ways, the most basic is the arrayOf() function
```Kotlin
// Creates an Array<Int> with values ["0", "1", "2", "3", "4"]
var ex1 = arrayOf(0,1,2,3,4)
// Creates an Array<String> with values ["0", "1", "4", "9", "16"]
val ex2 = Array(5, { i -> (i * i).toString() })
```
Individual elements are accessed by the '[ ]' operands
