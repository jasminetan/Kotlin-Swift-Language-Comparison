# Types 
## What types does the language support?
In Swift, there are two kinds of types 
1. Named types: can be given a particular name when it’s defined (classes, structures, enumerations, and protocols)
2. Compound types:  type without a name, defined in the Swift language itself (function types and tuple types)

### Tuple Type
A tuple type is a comma-separated list of types, enclosed in parentheses.
```Swift
var someTuple = (top: 10, bottom: 12)  // someTuple is of type (top: Int, bottom: Int)
someTuple = (top: 4, bottom: 42) // OK: names match
someTuple = (9, 99)              // OK: names are inferred
someTuple = (left: 5, right: 5)  // Error: names don't match
```
### Function Type
A function type represents the type of a function, method, or closure and consists of a parameter and return type separated by an arrow (->):

(parameter type) -> return type
### Both reference and value types supported.
### New value types be created.

## Type Inference
Swift uses type inference extensively, allowing you to omit the type or part of the type of many variables and expressions in your code. 

For example, instead of writing var x: Int = 0, you can write var x = 0, omitting the type completely—the compiler correctly infers that x names a value of type Int.

## Type Aliases
You can create a new name for an existing type using typealias
```Swift
typealias newname = type
```

### Optional Types: represent a variable that can hold either a value or no value.
These are equivalent:
```Swift
var optionalInteger: Int?
var optionalInteger: Optional<Int>
```
  
