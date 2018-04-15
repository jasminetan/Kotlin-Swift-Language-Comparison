Swift uses *automatic reference counting* to deal with garbage collection. Swift keeps track of how many references to an object there are during runtime, and if that number ever hits 0, it deallocates and removes the object. This usually works pretty well, but there are a few issues a developer should be aware of.

There's often a situation where one object--lets call it A--holds a reference to another object--B--but B also holds a reference to A at the same time. Since each object holds a reference to the other, their respective reference counts will always be at least 1, which means neither object will ever be deallocated, no matter if they're ever used again or not. This is called a **strong reference cycle**.

To combat this problem Swift has the `weak` keyword. The `weak` keyword is attached to a reference and tells Swift not to add this reference to the referred object's reference count. If there's a situation where a strong reference cycle can arise, using the `weak` keyword on either A or B's reference will make sure that the cycle is broken since at least one of A or B will have a reference count of 0 and will be deallocated.


