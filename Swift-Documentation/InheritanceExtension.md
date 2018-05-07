# Inheritance and Extension

To declare a subtype on a class you can either append a colon and supertype after the class header, or add it as an extension later.

ex: 
```
class MyClass: SuperClass {}
```
or:
```
class MyClass {}
extension MyClass: SuperClass {}
```

Overriding methods and properties is done with the override keyword. Overriding properties is mostly usefull to implement your own getter/setter or observer

Calling the superclass is done with the super keyword
