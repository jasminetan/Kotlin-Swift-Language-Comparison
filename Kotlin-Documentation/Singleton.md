Because Kotlin relies on the singleton pattern to implement static member functionality, creating singletons in Kotlin is extremely easy.

To create a singleton, simply use the `object` keyword:

      object ASingleton
      {
        //singleton code here
      }
 
That's all there is to it. 

The underlying Java code that `object ASingleton` generates is as follows:

```
public final class ASingleton {
   public static final ASingleton INSTANCE;

   private ASingleton() {
      INSTANCE = (ASingleton)this;
   }

   static {
      new ASingleton();
   }
}
```   
This is a well tested Java implementation for a lazily instantiated and thread-safe singleton.

As such, singletons in Kotlin are lazily instantiated and thread-safe by default.
