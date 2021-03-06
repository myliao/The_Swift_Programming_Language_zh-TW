# Swift 簡易教學

學習一個新程式語言大家做常寫的第一個程式應該就是在螢幕上印出 `Hello, World`。
在 Swift 中只需要一行程式碼：
```c
println("Hello, world")
```
如果您用過 C 或 Objective-C 進行程式開發，您應該會覺得上述的 Swift 語法相當熟悉，上述的範例中這一行程式碼已經是一個完整可獨立執行的程式。
您不需要 import `譯注1` 其他的函式庫或是額外的輸入/輸出字串處理 `譯注2`。

    譯注1: Objective-C 使用 #import "xxxxx.h" 來宣告使用其他函式庫的物件或函式 C 則使用 #include "xxxxx.h"

    譯注2: 可以參見章節[字串與字元]()

Code written at global scope is used as the entry point for the program, so you don’t need a main function. You also don’t need to write semicolons at the end of every statement.

This tour gives you enough information to start writing code in Swift by showing you how to accomplish a variety of programming tasks. Don’t worry if you don’t understand something—everything introduced in this tour is explained in detail in the rest of this book.

~~~
NOTE

For the best experience, open this chapter as a playground in Xcode. Playgrounds allow you to edit the code listings and see the result immediately.

[Open Playground](https://developer.apple.com/library/prerelease/ios/documentation/swift/conceptual/swift_programming_language/GuidedTour.playground.zip)
~~~

## Simple Values
Use let to make a constant and var to make a variable. The value of a constant doesn’t need to be known at compile time, but you must assign it a value exactly once. This means you can use constants to name a value that you determine once but use in many places.

```js
var myVariable = 42
myVariable = 50
let myConstant = 42
```

A constant or variable must have the same type as the value you want to assign to it. However, you don’t always have to write the type explicitly. Providing a value when you create a constant or variable lets the compiler infer its type. In the example above, the compiler infers that myVariable is an integer because its initial value is a integer.

If the initial value doesn’t provide enough information (or if there is no initial value), specify the type by writing it after the variable, separated by a colon.

~~~
let implicitInteger = 70
let implicitDouble = 70.0
let explicitDouble: Double = 70
~~~

~~~
EXPERIMENT

Create a constant with an explicit type of Float and a value of 4.
~~~

There’s an even simpler way to include values in strings: Write the value in parentheses, and write a backslash (\\) before the parentheses. For example:

~~~
let apples = 3
let oranges = 5
let appleSummary = "I have \(apples) apples."
let fruitSummary = "I have \(apples + oranges) pieces of fruit."
~~~

~~~
EXPERIMENT

Use \() to include a floating-point calculation in a string and to include someone’s name in a greeting.
~~~

Create arrays and dictionaries using brackets ([]), and access their elements by writing the index or key in brackets.

~~~
var shoppingList = ["catfish", "water", "tulips", "blue paint"]
shoppingList[1] = "bottle of water"

var occupations = [
    "Malcolm": "Captain",
    "Kaylee": "Mechanic",
]
occupations["Jayne"] = "Public Relations"
~~~

To create an empty array or dictionary, use the initializer syntax.

~~~
let emptyArray = String[]()
let emptyDictionary = Dictionary<String, Float>()
~~~

If type information can be inferred, you can write an empty array as [] and an empty dictionary as [:]—for example, when you set a new value for a variable or pass an argument to a function.

~~~
shoppingList = []   // Went shopping and bought everything.
~~~

## Control Flow

(待續)
