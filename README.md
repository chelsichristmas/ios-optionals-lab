# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```
Answer:
```
if let name = userNameOne {
print("The username is \(name)")
}

```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
```
Answer:
```
let userNameOne: String? = nil
let userNameTwo = userNameOne ?? "undefined"
print("The username is \(userNameTwo)")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
```
Answer:
```
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
rectOneWidth = 5
rectOneHeight = 10
if let width = rectOneWidth {
if let  height = rectOneHeight {
    print ("The area of rectOne is \(width * height)")
}
}

```
b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil

```
Answer:
```
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
var rectTwoArea : Double
if let width = rectTwoWidth,
  let height = rectTwoHeight {
    rectTwoArea = width * height
        print("The area is \(rectTwoArea)")
}  else {
    print("The area of rectTwo is not able to be calculated")
}

```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```
Answer:
```
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70

 if let name = userOneName,
let age = userOneAge,
    let height = userOneHeight {
    let heightInFeet = height / 12
    print("Hello \(name)! You are \(age) years old and \(heightInFeet).")
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```
Answer:
```
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
 if let name = userTwoName,
let age = userTwoAge,
let height = userTwoHeight {
    print("Hello \(name)! You are \(age) years old and \(height) feet tall.")
 } else {
    print ("Hello \(userTwoName ?? "user")! You are \(userTwoAge ?? 0) and I don't know how tall you are")
}
```

## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer:
```
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
if let number = favoriteNumber {
    print("Your favorite number is \(number)")
} else {
    print("I don't know you're favorite number")
}
```



## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer:
```
if let numberOne = numOne,
    let numberTwo = numTwo ,
    let numberThree = numThree {
    sum = (numberOne + numberTwo + numberThree)
    if sum != 0 {
        print("The sum of all the numbers is \(sum)")
    }
} else {
    print("The sum is 0")
}
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```
Answer:
```

```

b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
