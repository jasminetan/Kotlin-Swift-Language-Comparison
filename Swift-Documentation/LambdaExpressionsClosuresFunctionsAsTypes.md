#### Closures are self-contained blocks of functionality that can be passed around and used in your code. Closures in Swift are similar to blocks in C and Objective-C and to lambdas in other programming languages.

## Closure expressions
A closure expression creates a closure, also known as a lambda or an anonymous function
```Swift
{ (parameters) -> return type in
    statements
}
```

### Trailing Closures
If you need to pass a closure expression to a function as the function’s final argument and the closure expression is long, it can be useful to write it as a trailing closure instead.
```Swift
func someFunctionThatTakesAClosure(closure: () -> Void) {
    // function body goes here
}
 
// Here's how you call this function without using a trailing closure:
 
someFunctionThatTakesAClosure(closure: {
    // closure's body goes here
})
 
// Here's how you call this function with a trailing closure instead:
 
someFunctionThatTakesAClosure() {
    // trailing closure's body goes here
}
```
### Functions and closures are reference types
Whenever you assign a function or a closure to a constant or a variable, you are actually setting that constant or variable to be a reference to the function or closure
