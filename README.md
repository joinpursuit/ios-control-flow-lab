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
- C
- D

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
- It will give a compile-time error. case (_, 0.0..<1.0) should read case (_, 0.0...<1.0). The missing "." is a syntax error. If the additional "." is present, the console will print "\(appInfo.0) hasn't released yet". Since the first case condition is met, the program will not print the other switch cases or default case. 

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
- D. None of the cases include 4 in their range so the default case will run and print "D".

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

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```
switch currentWeather {
case ("rain"):
print ("Bring an umbrella and rain coat!")
case ("sunny"):
print ("Don't forget your shades!")
case ("snow"):
print ("Wear a warm hooded coat and snow boots!"
default: 
print ("What is the current weather? 'rain', 'snow', or 'sunny'?")
}
***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below
```
let fullName: String = firstName + " " + lastName

print (fullName)
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
var temperatureInFahrenheit: Int = 75
switch temperatureInFahrenheit {
case 0..<40 :
print("It's cold out.")
case 85..<1000 :
print("It's really warm.")
default:
    print("Weather is moderate.")
}

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
if (true == true) {
 print("You win!")
} 
else {
 print("You lose!")
}

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
switch numberOfSides {
case 3 :
print ("Triangle")
case 4 :
print ("Square")
case 5 :
print ("Pentagon")
case 6 :
print ("Hexagon")
case 7:
print ("Heptagon")
case 8:
print ("Octagon")
case 9:
print ("Nonagon")
case 10 :
print ("Decagon")
default:
print ("Error")
}

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
var grade: Int = 88

switch grade {
case 0..<65 :
print ("F")
case 65..<70 :
print ("D")
case 70..<79 :
print ("C")
case 80..<90 :
print ("B")
case 90..<100:
print ("A")
case 100:
print ("A+")
default:
print ("Error")
}

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
let firstName = "Peter"
var lastName: String = " "

if firstName == "Peter" {
 let lastName = "Gabriel"
} else if firstName == "Phil" {
 let lastName = "Collins"
}
let fullName = firstName + " " + lastName

The lastName variable is not declared outside scope of if statement. 
***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
let nameAndBirthYear: (String, Int) = ("Lorraine", 1992)
let age = 2019 - nameAndBirthYear.1

if age <= 10 {
    print ("You are in your preteen years.")
} else if age <= 19 {
    print ("You are in your teen years.")
} else if age <= 29 {
    print ("You are in your twenties.")
} else if age <= 39 {
    print ("You are in your thirties.")
} else if age <= 49 {
    print ("You are in your forties.")
} else if age <= 59 {
    print ("You are in your fifties.")
} else if age <= 69 {
    print ("You are in your sixties.")
} else if age <= 79 {
    print ("You are in your seventies.")
} else if age <= 89 {
    print ("You are in your eighties.")
} else if age <= 99 {
    print ("You are in your nineties.")
} else {
    print ("you're over 100.")
}

let nameAndBirthYear: (String, Int) = ("Lorraine", 1992)
let age = 2019 - nameAndBirthYear.1

switch age {
case 0..<10 :
 print ("You are in your preteen years.")
case 10..<19 :
 print ("You are in your teen years.")
case 19..<29 :
 print ("You are in your twenties.")
case 29..<39 :
 print ("You are in your thirties.")
case 39..<49 :
 print ("You are in your forties.")
case 49..<59 :
 print ("You are in your fifties.")
case 59..<69 :
 print ("You are in your sixties.")
case 69..<79 :
 print ("You are in your seventies.")
case 79..<89 :
 print ("You are in your eighties.")
case 89..<99 :
 print ("You are in your nineties.")
default:
 print ("you're over 100.")
}

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
My system would print "The answer to life, the universe and everything".

What happens when you change number to:

-a. 365?
My system would print "Days in a year"

-b. 1024?
My system would print "Bytes in a Kilobyte"

-c. 65?
My system would print "Some uninteresting number"

What happens when you remove the default clause?
The system would return a compile-time error. Switch statements must be exhaustive and the default clause ensures the code will cover every possibility.

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
a. 
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
} else if population > 5000 {
 message = "\(population) is a medium size town"
 }
 print (message)
b.  
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
} else if population > 5000 {
 message = "\(population) is a medium size town"
 } else {
  message = "\(population) is a mid-size town"
}
print (message)

c. 
var population: Int = 10000
switch population {
case 0..<5000 :
print ("\(population) is a mid-size town")
case 5000..<10000 :
print ("\(population) is a medium size town")
case 10000..<99999999999 :
print ("\(population) is a large town")
default:
print ("error")
}
***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional



b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
a.
let myTuple: (Int, Int) = (5, 10)
var sum = myTuple.0 + myTuple.1

if sum >= 15 {
    print ("Yes, the sum of the numbers in the tuple is at least 15.")
} else {
    print("No, the sum of the numbers in the tuple is less than 15.")
}

b.
let myTuple: (Int, Int) = (5, 10)
var sum = myTuple.0 + myTuple.1

switch sum {
    case 0..<15 :
        print ("No, the sum of the numbers in the tuple is less than 15.")
    case 15..<9999999 :
        print ("Yes, the sum of the numbers in the tuple is at least 15.")
    default:
    print ("Yes, the sum of the numbers in the tuple is at least 15.")
}

***
