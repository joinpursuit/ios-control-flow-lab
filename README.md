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

- A will be printed.
- B
- C will be printed.
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

- appInfo.0 hasn't released yet
- myCoolApp hasn't released yet -- This statement will be printed.
- Thanks for looking at myCoolApp! -- This statement will be printed.
- I'm not quite sure what you are looking at
- It will give a compile-time error

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
- D - This case would be printed.

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
- No default case in the switch statement - This is the error in the code.
- No print statement right outside the switch statement

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below

let currentWeather = "rain"

switch currentWeather{
case "rain":
    print("It's rainy out, make sure to grab an umbrella.")
case "snow":
    print("It's snowing out, make sure to wear a jacket.")
default:
print("It's sunny out! Enjoy the day.")
}

```

***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below

let firstName = "John"
let lastName = "Appleseed"

let fullName = firstName + " " + lastName

print("The Fellow's full name is \(fullName)")
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

let temperatureInFahrenheit: Int = 65

switch true {
case temperatureInFahrenheit <= 40 :
    print("It's cold out.")
case temperatureInFahrenheit >= 85 :
    print("It's really warm")
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
/*ANSWER
let userNum = 4

if 0..<5 ~= userNum{
    print("You win!")
} else {
    print("You lose!")
}
 */
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
/*ANSWER
var numberOfSides = 6

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
    print("Nonagon")
case 10:
    print("Decagon")
default:
    print("Error: Number out of range.")
}
*/
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
/*
var grade = 93

switch grade{
case 90..<100 :
    print("A")
case 80..<90 :
    print("B")
case 70..<80:
    print("C")
case 65..<70:
    print("D")
case 0..<65:
    print("F")
default:
    print("A+")
}
*/
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
/*ANSWER
-The variable lastName has isn't established and it needs to be mutable

let firstName = "Phil"
var lastName = "Gabriel"

if firstName == "Peter" {
 lastName = "Gabriel"
} else if firstName == "Phil" {
    lastName = "Collins"
}
let fullName = firstName + " " + lastName
*/

***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
/*ANSWER
//If statements
var nameAndBirthYear = (name: "Maitree", birthYear: 1989)


if nameAndBirthYear.birthYear >= 1999 && nameAndBirthYear.birthYear <= 2019{
    print("You are in your twenties")
} else if nameAndBirthYear.birthYear >= 1989 && nameAndBirthYear.birthYear <= 1999{
    print("You are in your thirties")
}else if nameAndBirthYear.birthYear >= 1979 && nameAndBirthYear.birthYear <= 1989{
    print("You are in your fourties")
}else if nameAndBirthYear.birthYear >= 1969 && nameAndBirthYear.birthYear <= 1979{
    print("You are in your fifties")
}

//Switch
var nameAndBirthYear = (name: "Maitree", birthYear: 1989)

switch nameAndBirthYear.birthYear {
case 1999...2019:
    print("You are in your twenties")
case 1989...1999:
    print("You are in your thirties")
case 1979...1989:
    print("You are in your fourties")
case 1969...1979:
    print("You are in your fifties")
default:
    print("Please enter age within range.")
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
 print("Some uninteresting number
 }
```
What happens when you change number to:

-a. 365?
This would print out "Days in a year"
-b. 1024?
This would print out "Bytes in a Kilobyte"
-c. 65?
This would print "Some interesting number"
What happens when you remove the default clause?
The code would not compile.
*/
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
/*ANSWER
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
} else if population < 10000 && population > 5000{
    print("It's a medium size town.")
} else {
    print("It's a mid-size town.")
}

//SWITCH STATEMENT

var population: Int = 10
var message = String()

switch true {
case population > 10000:
    print("\(population) is a large town")
case population < 5000 && population > 10000:
    print("It's a medium size town.")
default:
    print("It's a mid-size town.")
}



***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional

b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
***
/*ANSWER
let myTuple: (Int, Int) = (5, 10)

let sum = myTuple.0 + myTuple.1

if sum == 15 {
    print("The sum of the two numbers in the tuple is 15.")
    } else {
    print("The sum of the two numbers in the tuple is not 15.")
}

//SWITCH

let myTuple: (Int, Int) = (5, 10)

let sum = myTuple.0 + myTuple.1

switch true {
case sum == 15:
    print("The sum of the two numbers in the tuple is 15.")
default:
    print("The sum of the two numbers in the tuple is not 15.")
}
*/
