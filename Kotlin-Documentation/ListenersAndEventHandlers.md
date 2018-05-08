#Listeners and Handlers

Listeners wait and watch for events to be fired. In Kotlin the objects who do the listening are often the same ones that handle them. Below is an example: 

```Kotlin
exitScreen.setOnClickListener(object : Screen.OnClickListener { 
    override fun onClick(v: View?) { 
        close()
    }
})
```

The above function adds an on click listeners to the **exitScreen** object. After 
checking if null the overidden **onClick** function calls another function called **close()** where the request is handled. Here the method **onClick()** acts as the events handler.
