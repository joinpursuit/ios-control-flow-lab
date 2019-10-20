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

- (A)
- B
- (C)
- (D)

***
```
Answer

```swift

will print C and D
```
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

***
```
ANSWER
      ```swift
Will print "myCoolApp hasn't released yet."
```
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
- (D)      Will print D

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
- (No default case in the switch statement) ---Answer
- No print statement right outside the switch statement

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```
ANSWER
```swift

let currentWeather = "rain"
switch currentWeather {
case "snow" :
print("BUUUURRRRRRRR IT'S COLD IN HERE🥶🥶🥶")
case "rain" :
print("It's raining 🌧, it's pouring💦, the old man is snoring👴🏾💤")
case "sunny" :
print("EVERYBODY'S GOT A LITTLE LIGHT UNDER THE SUN, UNDER THE SUN, UNDER THE SUN, UND......")
default:
print("Watch Fox News")
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
ANSWER
```swift

let firstName = "John"
let lastName = " Appleseed"

let fullName = firstName + lastName
print("The Fellow's full name is \(fullName).")
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
ANSWER
```swift

var temperatureInFahrenheit = 60
switch true {
case temperatureInFahrenheit <= 40 :
print("It's cold out!")
case temperatureInFahrenheit >= 85 :
    print("It's really warm")
default:
print("Weather is moderate")
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
ANSWER
```swift

var points = 102
if points >= 100 {
 print("You win!")
}
else {
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
ANSWER
```swift
var numberOfSides = 6

switch numberOfSides {
case 1 :
print("Error")
case 2 :
print("Error")
case 3 :
print("Triangle")
case 4 :
print("Square")
case 5 :
print("Pentagon")
case 6 :
print("Hexagon")
case 7 :
print("Heptagon")
case 8 :
print("Octagon")
case 9 :
print("Enneagon")
case 10 :
print("Decagon")
default :
    print("Enter number")
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
ANSWER
```swift

var gradePointAverage = 87
switch gradePointAverage {
case 100 :
    print("A+")
case 90...99 :
    print("A")
case 80...89 :
    print("B")
case 70...79 :
    print("C")
case 65...69 :
    print("D")
case 0..<65 :
    print("F")
default:
    print("Course is Incomplete")
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
ANSWER
```swift

let firstName1 = "Peter"
var lastName1 = ""

if firstName1 == "Peter" {
 lastName1 = "Gabriel"
} else if firstName1 == "Phil" {
  lastName1 = "Collins"
}
let fullName1 = firstName1 + " " + lastName1

```
***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
ANSWER
```swift

let nameAndBirthYear = (name: "Andi", birthYear: 1994)

switch nameAndBirthYear {
case (_, 1970..<1980):
    print("Hi \(nameAndBirthYear.name), you are in your fourties!")
case (_, 1980..<1990):
    print("Hi \(nameAndBirthYear.name), you are in your thirties!")
case (_, 1990..<2000):
     print("Hi \(nameAndBirthYear.name), you are in your twenties!")
case (_, 2000..<2010):
     print("Hi \(nameAndBirthYear.name), you are a teen!")
case (_, 2010..<2020):
     print("Hi \(nameAndBirthYear.name), you're too young to care about any of this.")
default:
     print("Hi \(nameAndBirthYear.name), you're old as dirt.")
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
ANSWER
```swift

"The answer to life, the universe and everything"
```
What happens when you change number to:

-a. 365?
 console will print "days in a year"

-b. 1024?
 console will print "Bytes in a Kilobyte"
 
-c. 65?
console will print the default statement "Some uninteresting number"

What happens when you remove the default clause?
 the code will not compile without a default clause at the end of a switch statement                  
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
ANSWER
```switch
if/else:

var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
 } else if population < 10000 && population > 5000 {
    message = "\(population) is a medium sized town"
 } else {
 message = "\(population) is a medium sized town."
 }
 
switch:

var population: Int = 10000
var message = String()

switch population {
case 10_000..<100_000 :
    message = "\(population) is a large town."
case 5_001..<10_000 :
     message = "\(population) is a medium sized town."
default :
     message = "\(population) is a mid sized town."
}
print(message)
```
***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional

b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
ANSWER
```swift
if/else:

let myTuple: (Int, Int) = (5, 10)
let sumOfMyTuple = myTuple.0 + myTuple.1
if sumOfMyTuple >= 15 {
    print("The sum of my tuple is at least 15.")
} else {
    print("The sum of my tuple is less than 15.")
}

switch:

switch sumOfMyTuple {
case 0..<15 :
    message = "The sum of my tuple is less than 15."
case 15..<100_000 :
    message = "The sum of my tuple is at least 15."
default :
    message = "I'm not sure if the sum of my tuple is at least 15."
    }
```
***
