# Properties

## Declaring Properties
Properties in swift are declared using the mutable keyword **var** or the read-only **val**

```swift
class SomeClass{
  var person = ...
  var place = ...
  var thing = ...
}
```
To use a property we can simply refer to it by its name

```swift
val Persona = SomeClass()
Persona.person = "Duck"
Persona.place = "Pond"
Persona.thing = "Bread"
```
## Getter and Setter
Getter and Setter functions can be implemented in Kotlin as well. Below is an example property with getter and setter methods
By convention the setter parameter name is **value**
```swift
  var age : Int?
    get() = this.age
    set(value) { 
      this.age = value
    }
```
Kotlin also supports the use of backed variables with implicit and explicit definitions. 
