Getters and setters…write your own or built in?
Backing variables?
Computed properties?

Swift builds in getters, setters, as well as observers to properties.

Here's an example:

```swift
struct Person {
  var name: String {
    get {
      if name.count == 0 {
        return "No Name"
      } else {
        return name
      }
    }
    set {
      name = "My name is: \(newValue)"
    }
```

if you remove the get keyword and just implement the logic inside curly braces, you'll have a read-only computed property

along with get and set, the observers willSet and didSet allow you to perform actions when the property is about to be changed and when it has been changed
