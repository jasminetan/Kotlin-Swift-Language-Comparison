# Interfaces

Interfaces in Kotlin mainly are containers of abstract methods, and sometimes method implementations.  The difference between these and abstracted classes is that interfaces cannot store state, and any properties they have need to be abstract.

Interfaces are defined using the 'interface' keyword.
```Kotlin
interface ExampleInterface {
    fun ex1()
    fun ex2(){
        println("This body code is optional")
    }
}
```

Classes in Kotlin can **implement** any number of interfaces, and the functions are all overriden as normal.  If more than one function has the same function header it is possible to override both separately using the 'super' keyword to denote each.
```Kotlin
class ExampleClass : InterfaceOne, InterfaceTwo {
    override fun ex1() {
        println("From interface one")
    }
    override fun ex2() {
        println("From interface two")
    }
    override fun shared() {
        super<InterfaceOne>.shared()
        super<InterfaceTwo>.shared()
     }
}
```

**Properties** in interfaces can be abstract or give implimentations for accessors.
```Kotlin
interface ExampleInterface {
    var x: String
    var y

    var zWithImplimentation: String
        get() = "value"
}
```
