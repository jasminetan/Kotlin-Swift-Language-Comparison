Does the language have any particularly unique features?

Swift has automatic reference counting which means it tracks the number of references currently pointing to every object. This means that when, and only when, you're fully done with an object will the memory be deallocated. This can potentially cause problems where two objects reference each other, but this is solved with the `weak` keyword telling the compiler to skip counting that reference.

Swift also features strong typing and concise definitions, allowing for more readable code that's less prone to errors.

Optional types are fantastic for effectively eliminating null references. You can still get them if you try hard, but the language does what it can to stop you from shooting yourself in the foot.
