## Swift supports **Protocols** 
### What abilities does it have?
Protocols define a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality.

### How is it used?
You define protocols in a very similar way to classes, structures, and enumerations:
```Swift
protocol SomeProtocol {
    // protocol definition goes here
}
```
The protocol can then be adopted by a class, structure, or enumeration to provide an actual implementation of those requirements. Any type that satisfies the requirements of a protocol is said to conform to that protocol.

In addition to specifying requirements that conforming types must implement, you can extend a protocol to implement some of these requirements or to implement additional functionality that conforming types can take advantage of.

