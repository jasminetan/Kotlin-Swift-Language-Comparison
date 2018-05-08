Threads or thread-like abilities
How is multitasking accomplished?

# Multithreading
Kotlin usage is based mostly on the framework of Java. Since java offers multithreading natively, Kotlin uses a simple API to intialize and run threads.
```kotlin
fun thread(
        start: Boolean = true, // If true, the thread is immediately started.
        isDaemon: Boolean = false, //  If true, the thread is created as a daemon thread.
        contextClassLoader: ClassLoader? = null, // The class loader to use for loading classes and resources in this thread.
        name: String? = null, // Name of the thread.
        priority: Int = -1, // Priority of the thread.
        block: () -> Unit // Block of code to run.
): Thread (source)
```
Similar to Java **run()**, block acts as the location for code to be run during the threads execution.
The thread can be instantiated using the sytax below. 
```kotlin
thread() {
    println("Go craaaaaaaaaaazy :D")
}
```
