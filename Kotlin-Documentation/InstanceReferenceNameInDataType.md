# 'This' Keyword

The 'this' keyword in Kotlin is used to represent the current instance reference.
```Kotlin
// For example the 'this' keyword below is denoting the class it was called in
class Test {
    fun sendThis() {
        return this
    }
}
```

You can also specify a more specific scope on the 'this' keyword using 'this@label' and replace 'label' with the scope you intend.
```Kotlin
class Upper {
    inner class Lower {
        fun sendUpper {
            return this@sendUpper
        }
        fun sendLower {
            return this@Lower
        }
    }
}
```
