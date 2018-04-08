# Classes
## Defining
Classes are defined with the keyword **class** and standard Swift types use *UpperCamelCase* names
```swift
class SomeClass{

}
```
## Creating new instances
```swift
let SomeClass = Class()
```

## Constructing/initializing

Initializers in swift are written using the **init** keyword
```swift
init() {
    // perform some initialization here
}
```


## Destructing/de-initializing
You write deinitializers with the **deinit** keyword. Deinitializers are only available on class types.

Swift automatically deallocates your instances when they are no longer needed, to free up resources. Typically you don’t need to perform manual cleanup when your instances are deallocated. However, when you are working with your own resources, you might need to perform some additional cleanup yourself.

```swift
deinit {
    // perform the deinitialization
}
```
Deinitializers are called automatically, just before instance deallocation takes place. You are not allowed to call a deinitializer yourself. 
