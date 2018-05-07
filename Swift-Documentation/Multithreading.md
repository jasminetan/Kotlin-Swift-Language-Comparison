Threads or thread-like abilities
How is multitasking accomplished?

There are a few ways to use multithreading in swift.

The first is with the Process class. This will create a new child process independent of the parent process but containing all the information the parent had at the time of the process's creation.

Then there's the Thread class, which is similar to a Process but shares memory with the parent process. This of course can cause issues with concurrent modification of objects.

Also DispatchQueues. These can take in tsaks and execute them in order, but with multiple queues on different threads we can achieve concurrent operation of queued tasks
