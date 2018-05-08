# Lamda Expressions and Higher Order Functions
Kotlin functions are considered first class members. Meaning they can be stored in variables and passed to other functions in a similar manner.
## Higher Order Functions
A higher order functions is one that takes a functions as a parameter or returns a functions as a result

```kotlin
fun <T, R> Collection<T>.fold(
    initial: R, 
    combine: (acc: R, nextElement: T) -> R
): R {
    var accumulator: R = initial
    for (element: T in this) {
        accumulator = combine(accumulator, element)
    }
    return accumulator
}
```

Above the function combine takes the parameters of type R and T and returns type R. As a higher order function it takes in a function/val of type T and calls  the combine method on each memeber of the collection. Something that is only possible with the ability to pass and return functions.

## Lamda Expressions
Lamda functions are not named or declared but instead passed immediately as an expression. Lamba epressions are surrounded by **{}** brackets intantiated like so

```swift
maxValue("stuff", {a , b -> a.value > b.value})
```

The function maxValue is a higher order functin that takes in two parameters, the first being the string "stuff", and the second being a function. 
