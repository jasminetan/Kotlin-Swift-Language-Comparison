Kotlin does have a `null` value, but also implements several null safety features to help prevent the very common NullReferenceException error.

Kotlin's null safety revolves around the existence of nullable references (references that can hold `null`) and non-null references (references that cannot hold `null`)

By default, all references are non-null. You can declare a reference nullable with the `?` operator:

      var nullableVar: String? = "abc"
      
If you attempt to access members or methods of an object in a nullable reference, you'll get an error at compile time. This is because Kotlin has not verified that the object being referenced is in fact not null.

      var nullableVar: String? = "abc"
      val l = nullableVar.length //this throws a compiler error
      
Verifying that a nullable reference is not null can be done in several ways:

* Explicity, using conditions

  You can use conditions to check for null first before attempting to access the reference.

      val l = if (nullableVar != null) nullableVar.length else -1
    
* Safe Calls

  The `?` operator can also be used to create a 'safe call', a call to an object's member that first checks if the object is null. If it   is null, then the call returns the `null` value, thereby allowing the program to continue executing.
  
      val l = nullableVar?.length
      
* Elvis Operator

  The elvis operator, `?:`, is used to define two expressions that can be used depending on whether another expression is null.
  
      var a = nullableVar ?: -1
      
  The above code with assign `nullableVar` to `a` only if `nullableVar` is null. Otherwise, `a` is assigned `-1`.
      
  
* !! Operator

  The `!!` operator throws null safety out the window. This operator converts any value to a non-null type and throws a      NullReferenceException error if the value is null.
  
      val b = nullableVar!!.length //will throw runtime NPE error if nullableVar is null!
      
 
