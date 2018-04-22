## What reflection abilities are supported?
Swift reflection allows us to look at objects' properties without modifying them. This concept is called a **mirror**.

A **mirror** describes the parts that make up a particular instance, such as the instance’s stored properties, collection or tuple elements, or its active enumeration case. Mirrors also provide a “display style” property that suggests how this mirror might be rendered.
## How is reflection used?

Playgrounds and the debugger use the Mirror type to display representations of values of any type. For example, when you pass an instance to the dump(_:_:_:_:) function, a mirror is used to render that instance’s runtime contents.
```Swift
struct Point {
    let x: Int, y: Int
}

let p = Point(x: 21, y: 30)
print(String(reflecting: p))
// Prints "▿ Point
//           - x: 21
//           - y: 30"
```
