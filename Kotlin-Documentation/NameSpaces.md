Although Kotlin does not strictly have Namespaces, it does have a very similar construct, called **Packages**. Packages in Kotlin are used to bundle up the classes and functions of a source file for use in another file.

To create a package, use the *package* keyword followed by its name:

        
    package foo.bar

    fun pop() {}

    class Dog {}
        
        
Packages can contain other packages. In the above example, we have created the `bar` package, which is contained inside the `foo` package.

We can access the classes and functions of this package inside another file using the `import` statement:

    import foo.bar.*
    
The asterisk is a wildcard that imports every class and function in `foo.bar`.

We can also selectively import only certain functions or classes:

    import foo.bar.pop
    import foo.bar.Dog
    
And finally, aliases can be created using the `as` keyword:

    import foo.bar.pop as popFun
    
This is useful for avoiding conflicts between two imported functions that have the same name.
