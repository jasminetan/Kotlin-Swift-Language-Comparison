Singletons in Swift are almost as easy as they are in Kotlin, and are also thread-safe and lazily instantiated.

```
class ASingleton {
    static let sharedInstance = ASingleton()
}
```
