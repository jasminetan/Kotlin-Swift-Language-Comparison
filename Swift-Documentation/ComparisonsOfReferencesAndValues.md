# How are values compared? (i.e. comparing two strings) 
## Swift supports all standard C comparison operators

- Equal to (a == b)

- Not equal to (a != b)

- Greater than (a > b)

- Less than (a < b)

- Greater than or equal to (a >= b)

- Less than or equal to (a <= b)

Each of the comparison operators returns a Bool value to indicate whether or not the statement is true:

```swift
1 == 1   // true because 1 is equal to 1
2 != 1   // true because 2 is not equal to 1
2 > 1    // true because 2 is greater than 1
1 < 2    // true because 1 is less than 2
1 >= 1   // true because 1 is greater than or equal to 1
2 <= 1   // false because 2 is not less than or equal to 1
```

## Comparing strings
Swift provides three ways to compare textual values: 
1. String and character equality
String and character equality is checked with the “equal to” operator (==) and the “not equal to” operator (!=)

*Note: Two String values (or two Character values) are considered equal if their extended grapheme clusters are canonically equivalent.* 
```swift 
// "Voulez-vous un café?" using LATIN SMALL LETTER E WITH ACUTE
let eAcuteQuestion = "Voulez-vous un caf\u{E9}?"
 
// "Voulez-vous un café?" using LATIN SMALL LETTER E and COMBINING ACUTE ACCENT
let combinedEAcuteQuestion = "Voulez-vous un caf\u{65}\u{301}?"
 
if eAcuteQuestion == combinedEAcuteQuestion {
    print("These two strings are considered equal")
}
// Prints "These two strings are considered equal"
```
2. Prefix equality
To check whether a string has a particular string prefix or suffix, call the string’s hasPrefix(_:) 
3. Suffix equality 
To check whether a string has a particular string prefix or suffix, call the string’s hasSuffix(_:) 
## Comparing references
Swift also provides two identity operators (=== and !==), which you use to test whether two object references both refer to the same object instance
