# Errors and exception handling
In Swift, errors are represented by values of types that conform to the **Error** protocol. This empty protocol indicates that a type can be used for error handling.

Error handling in Swift resembles exception handling in other languages, with the use of the try, catch and throw keywords. Unlike exception handling in many languages—including Objective-C—error handling in Swift does not involve unwinding the call stack, a process that can be computationally expensive. As such, the performance characteristics of a throw statement are comparable to those of a return statement.


There are four ways to handle errors in Swift. 
1. You can propagate the error from a function to the code that calls that function
```swift
func canThrowErrors() throws -> String
```
2. Handle the error using a do-catch statement
```swift
do {
    try expression
    statements
} catch pattern 1 {
    statements
} catch pattern2 where condition {
    statements
} catch {
    statements
}
```
3. Handle the error as an optional value

You use **try?** to handle an error by converting it to an optional value.
```swift
func someThrowingFunction() throws -> Int {
    // ...
}
let x = try? someThrowingFunction()
let y: Int?
do {
    y = try someThrowingFunction()
} catch {
    y = nil
}
```
4. Assert that the error will not occur. 

Write try! before the expression to disable error propagation and wrap the call in a runtime assertion that no error will be thrown.
```swift
let photo = try! loadImage(atPath: "./Resources/John Appleseed.jpg")
```

