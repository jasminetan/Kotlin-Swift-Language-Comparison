Which does the language use? (null/nil/etc)
Does the language have features for handling null/nil references?

Swift uses `nil` 

For handling `nil` you must use Optional Chaining. Optional chaining is a process for querying and calling properties, methods, and subscripts on an optional that might currently be `nil`. If the optional contains a value, the property, method, or subscript call succeeds; if the optional is `nil`, the property, method, or subscript call returns `nil`. Multiple queries can be chained together, and the entire chain fails gracefully if any link in the chain is `nil`.