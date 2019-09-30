# Control Flow Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

What will be printed when the code below is run?  Select all that apply.

```swift
let conditionOne = !(4 < 5) || !(3 > 8)
let conditionTwo = !(!true)

if conditionOne {
 print("A")
} else if conditionTwo {
 print("B")
}
if conditionTwo {
 print("C")
}
print("D")
```

- A
- B
- C
- D

Answer
```swift
A
C
D

```

***
## Question 2

What will the code block below print?  Select all that apply:

```swift
let appInfo = (name: "myCoolApp", version: 0.4)
switch appInfo {
 case (_, 0.0..<1.0):
 print("\(appInfo.0) hasn't released yet")
 case ("myCoolApp", _):
 print("Thanks for looking at myCoolApp!")
 default:
 print("I'm not quite sure what you are looking at")
}
```

- appInfo.0 hasn't released yet
- myCoolApp hasn't released yet
- Thanks for looking at myCoolApp!
- I'm not quite sure what you are looking at
- It will give a compile-time error

Answer
```swift
- myCoolApp hasn't released yet

```
***
## Question 3

What will be printed to the console when the code below is run?  Select all that apply.

```swift
let x: Int = 4
switch x {
case 0..<4:
 print("A")
case 5..<10:
 print("B")
case is Double:
 print("C")
default:
 print("D")
}
```

- A
- B
- C
- D

Answer
```swift
D

```
***
## Question 4

What are the errors in the code below for the switch statement? Select all that apply.

```swift
let candyType : String = "skittles"

switch candyType {
case "mAndM":
 print("Melts in your mouth, not in your hand")
case "skittles":
 print("Taste the rainbow")
case "snickers":
 print("Hungry? Grab a Snickers")
}
```

- No parentheses around the conditions
- No opening and closing brackets in each of the cases
- No default case in the switch statement
- No print statement right outside the switch statement

Answer
```swift
- No default case in the switch statement

```
***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```
Answer
```swift
let currentWeather = "rain"

switch currentWeather {
case "rain":
    print("It's rainy today")
case "sunny":
    print("It's a nice weather today")
case "snow":
    print("It's snowing today")
default:
    print("I'm not sure what's the weather today")
}

```

***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below
```
Answer
```swift
let firstName = "John"
let lastName = "Appleseed"
var fullName = "\(firstName) \(lastName)" 

print(fullName)
```

***

## Question 7

Convert the if/else statement below into a switch statement.

```swift
if temperatureInFahrenheit <= 40 {
 print("It's cold out.")
} else if temperatureInFahrenheit >= 85 {
 print("It's really warm.")
} else {
 print("Weather is moderate.")
}

//Re-written statement here

```
Answer
```swift
switch temperatureInFahrenheit {
case 0..<40:
    print("It's cold out.")
case 85...:
    print("It's really warm.")
default:
    print("Weather is moderate.")
}

```

***

## Question 8

Complete the following code so that "You win!" is printed.

```swift
if {
 print("You win!")
} 
else {
 print("You lose!")
}
```
Answer
```swift
var result = "win"

if result == "win"{
 print("You win!")
} else {
 print("You lose!")
}


```
***

## Question 9

Given a variable called numberOfSides, write code using a switch so that it prints out the name of the shape. Account for shapes with 3 to 10 sides and print an error message if out of range.

var numberOfSides = 6

```swift
Example 1:

Input:
var numberOfSides = 4

Output:
Square

Example 2:

Input:
var numberOfSides = 2

Output:
Error

```
Answer
```swift
var numberOfSides = 4

switch numberOfSides {
case 3:
    print("Triangle")
case 4:
    print("Square")
case 5:
    print("Pentagon")
case 6:
    print("Hexagon")
case 7:
    print("Heptagon")
case 8:
    print("Octagon")
case 9:
    print("Decagon")
case 10:
    print("Polygon Song")
default:
    print("Error")
}

```
***

## Question 10

Create a switch statement that will convert a number grade into a letter grade as shown below:

```swift
Numeric Score 	Letter Grade
100 	A+
90 - 99	A
80 - 89	B
70 - 79 	C
65 - 69 	D
Below 65 	F
```
Answer
```swift
var numericScore = 100

switch numericScore {
case 100...:
    print("A+")
case 90...99: 
    print("A")
case 80...89:
    print("B")
case 70...79:
    print("C")
case 60...69:
    print("D")
default:
    print("F")
} 

```
***

## Question 11

What is wrong with the block of code below?  Correct it so it behaves as expected.

```swift
let firstName = "Peter"

if firstName == "Peter" {
 let lastName = "Gabriel"
} else if firstName == "Phil" {
 let lastName = "Collins"
}
let fullName = firstName + " " + lastName
```
Answer
```swift
let firstName = "Peter"
let lastName: String

if firstName == "Peter" {
 lastName = "Gabriel"
} else if firstName == "Phil" {
 lastName = "Collins"
} else {
    lastName = ""
}

let fullName = firstName + " " + lastName

```
***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
Answer
```swift
let nameAndBirthYear = (name: "Eddie", birthYear: 1998)

if nameAndBirthYear.birthYear > 2000 {
    print("You are young")
} else if nameAndBirthYear.birthYear <= 1999 && nameAndBirthYear.birthYear >= 1990  {
    print("You are in your twenties")
} else if nameAndBirthYear.birthYear <= 1989 && nameAndBirthYear.birthYear >= 1980 {
    print("You are in your thirties")
} else if nameAndBirthYear.birthYear <= 1979 && nameAndBirthYear.birthYear >= 1970 {
    print("You are in your fourties")
} else {
    print("You're old")
}

switch nameAndBirthYear.birthYear {
case 2000...:
    print("You are young")
case 1990...1999:
    print("You are in your twenties")
case 1980...1989:
    print("You are in your thirties")
case 1970...1979:
    print("You are in your fourties")
default:
    print("You're old")
}

```
***


## Question 13

Consider the below switch statement. What should your system currently print?

```swift
let number = 42

switch number {
case 365:
 print("Days in year")
case 1024:
 print("Bytes in a Kilobyte")
case 0:
 print("Where arrays start")
case 42:
 print("The answer to life, the universe and everything")
default:
 print("Some uninteresting number")
```
What happens when you change number to:

-a. 365?

-b. 1024?

-c. 65?

What happens when you remove the default clause?

Answer - What happens when you change number to:
```swift
-a. 365?
    - prints "Days in year"
-b. 1024?
    - prints "Bytes in a Kilobyte"
-c. 65?
    - prints "Some uninteresting number"
```
Answer - What happens when you remove the default clause?
```swift
You'll recieve an error message saying that "Switch must have exhaustive"

```
***


## Question 14

Consider the variable below called population and the if-condition.

a. Add an else-if-condition that states if population is less than 10000 but greater than 5000, then message changes to say it's "a medium size town".

b. Add an else-condition where message changes to say it's a mid-size town.

c. Convert your final if-else statement to a switch statement.

```swift
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
}
```
Answer
```swift
var population: Int = 10000
var message = String()

if population > 10000 {
    message = "\(population) is a large town"
 } else if population > 5000 && population > 10000 {
    message = "\(population) is a medium size town"
 } else {
    message = "it's a mid-size town"
}
 
 switch population {
 case 10000...:
    message = "\(population) is a large town"
 case 5000...10000:
    message = "\(population) is a medium size town"
 default:
  message = "it's a mid-size town"
}

```
***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional

b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
Answer
```swift
let myTuple: (Int, Int) = (5, 10)

if myTuple.0 + myTuple.1 > 15 {
    print("sum of the two numbers in the tuple is at least 15")
} else {
    print("sum of the two numbers in the tuple is lower than 15")
}


switch mymyTuple {
case myTuple.0 + myTuple.1 > 15:
    print("sum of the two numbers in the tuple is at least 15")
default:
    print("sum of the two numbers in the tuple is lower than 15")
} 
```
***
