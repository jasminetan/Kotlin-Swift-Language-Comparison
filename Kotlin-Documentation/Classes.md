# Classes

## Creation
Classes are defined using the keyword 'class'
```kotlin
class Dog {

}
```

## Constructors / Initializers
Classes can have a primary constructor as well as secondary constructors.  Primary constructors are included in the class header as follows
```kotlin
class Dog(breed: String) {

}
```
**Primary Constructors** may not contain any code, this should be placed in an initializer block as follows
```kotlin
class Dog(breed: String) {
    init {
        println("The breed is ${breed}")
    }
}
```
You can also declare properties from within the primary constructor with val and var as follows
```kotlin
class Dog(val breed: String, var name: String, var age: Int) {

}
```
**Secondary Constructors** can be declared with the keyword 'constructor' as follows
```kotlin
class Dog {
    constructor(name: String) {
        println("The name is ${name}")
    }
}
```
Note that 'init' blocks will always execute before secondary constructors as they are more or less tied to the primary constructor.

## New instances
To create instances of a class, just call the constructor as a regular function, no need for a 'new' keyword
```kotlin
var newDog = Dog()
var namedDog = Dog("Steve")
```

## Deconstructing / De-initializing
Kotlin does not support deconstructing or de-initializing classes
