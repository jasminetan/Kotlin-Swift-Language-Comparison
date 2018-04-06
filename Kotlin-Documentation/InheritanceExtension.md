# Inheritance and Extension

To declare a supertype on a class, place a colon and the supertype after the class header.

*NOTE* : All classes are declared 'final' by defualt, thus all supertypes must have the keyword 'open'
```kotlin
open class Parent(x: Int)
class Child(x: Int) : Parent(x)
```
If the parent class has a primary constructor, the child class must be intialized using the parameters of this primary constructor.

If the child class does not have a primary constructor, each secondary constructor has to intitialize the base type using the 'super' keyword
```kotlin
class Child {
    constructor(x: Int) : super(x)
}
```

**Overriding Methods** is done using the keyword 'override'.
Overridable methods are similar to extendable classes in the fact that they have to be explicitly extendable with the keyword 'open'
```kotlin
open class Parent {
    open fun run() {}
}
class Child() : Parent() {
    override fun run() {}
}
```

**Overriding Properties** works the same way as overriding methods.
```kotlin
open class Parent {
    open val x = 1
}
class Child() : Parent() {
    override val x = 2
}
```

**Calling the Superclass** is done with the 'super' keyword
```kotlin
open class Parent {
    open fun test() { println("test") }
}

class Child : Parent() {
    override fun test() {
        super.test()
        super.test()
        super.test()
    }
}
```
