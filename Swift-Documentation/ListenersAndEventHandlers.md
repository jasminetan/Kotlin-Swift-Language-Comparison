#Listeners and Event Handlers
Swift implements a few different design patterns when handling events. Below is an classic exaple of how evets are recognized and handled between two objects.

```swift
class Kid {
    let events = EventManager();

    func yell() {
        println("Kid: ALALALAALALALALAALALOOOOO");
        self.events.trigger("yell", information: "This kid is nuts!");
    }
}
```

The above class can trigger an event called **yell** with the information "This kid is nuts!"

```swift
class Adult {
    func helpOut(kid:Kid) {
        // you can pass in an anonymous code block to the event listener
        kid.events.listenTo("yell", action: {
            println("Adult: Uhhhh, wheres you're mom?");
        });
        
        // Using the information from the trigger:
        kid.events.listenTo("yell", action: self.whyMe);
    }

    func whyMe(information:Any?) {
        if let info = information as? String {
            println("This kid is nuts!");
            println("I'm just gonna go...");
        }
    }
}
```

The above class Adult adds a **listener** to the kid passed as a parameter. Depending on the action type and information the adult responds differently to the tirgger and **handles** the request. 
