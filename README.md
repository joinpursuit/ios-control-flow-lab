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
let conditionOne = !(4 < 5) || !(3 > 8) // ConditionOne = True
let conditionTwo = !(!true) // True

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

/* Question #1 Answer

A, C, and D will all be printed when the code is run.

*/

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

/* Question #2 Answer

What will be printed is, myCoolApp hasn't released yet.

*/
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

/* Question #3 Answer

D will be printed to the console.

*/
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

/* Question #4 Answer

The only error in this code is the lack of a default case.

*/
***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```
/* Question #5 Answer

switch currentWeather{

case "rain":
print("It is highly recommended that you bring along an umbrella today.")
case "sunny":
    print("Rejoice, for you will have no need of an umbrella today!")
case "snow":
    print("It will snow today.")
default:
    print("")
}

*/
***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below
```
/* Question #6 Answer //THE WORDING IS UNUSUAL HERE. ASK A QUESTION ABOUT WHAT IS EXPECTED.

let fullName: String
fullName = firstName + " " + lastName"
print("The Fellow's full name is \(fullName).")

*/
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
/* Question #7 Answer

Assuming temperatureInFahrenheit is some Integer variable or constant that is already defined.

switch temperatureInFahrenheit{

case ...40:
    print("It is cold out.")
    
case 85...:
    print("It is really warm.")
    
default:
    print("Weather is moderate.")
    
}

*/
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
/* Question #8 Answer

if (true) {
 print("You win!")
} 
else {
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
/* Question #9 Answer

Example 1:

var numberOfSides = 4

switch numberOfSides{
case 0..<3:
    print("Error")
case 3:
    print("Triangle")
case 4:
    print("Square (Quadrilateral)")
case 5:
    print("Pentagon")
case 6:
    print("Hexagon")
case 7:
    print("Septagon")
case 8:
    print("Octagon")
case 9:
    print("Nonagon")
case 10:
    print("Decagon")
default:
    print("Error")
}

Example 2:

var numberOfSides = 2

switch numberOfSides{
case 0..<3:
    print("Error")
case 3:
    print("Triangle")
case 4:
    print("Square (Quadrilateral)")
case 5:
    print("Pentagon")
case 6:
    print("Hexagon")
case 7:
    print("Septagon")
case 8:
    print("Octagon")
case 9:
    print("Nonagon")
case 10:
    print("Decagon")
default:
    print("Error")
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
/* Question #10 Answer

var numberGrade: Double

switch numberGrade{
case ..<65:
    print("F")
case 65...69:
    print("D")
case 70...79:
    print("C")
case 80...89:
    print("B")
case 90...99:
    print("A")
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
/* Question #11 Answer
The last line is problematic because the compiler sees it and doesn't see a "lastName" variable that has been defined within the global scope. The constant lastName is conditionally defined within the scope of the if/else block.

let firstName = "Peter"
var lastName = ""

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
/* Question #12 Answer //ASK IF BIRTHYEAR OR AGE

Assuming that I am given a birthyear and not an explicit age.

if( nameAndBirthYear.1 <= 2019 && nameAndBirthYear >= 2010 ) {

    print("You are between 0 and 9 years of age.")
    
} else if( nameAndBirthYear.1 <= 2009 && nameAndBirthYear.1 >=  2000 ){

    print("You are between 10 and 19 years of age.")
    
} else if( nameAndBirthYear.1 <= 1999 && nameAndBirthYear.1 >=  1990 ){

    print("You are in your twenties.")
    
} else if( nameAndBirthYear.1 <= 1989 && nameAndBirthYear.1 >=  1980 ){

    print("You are in your thirties.")
    
} else if( nameAndBirthYear.1 <= 1979 && nameAndBirthYear.1 >=  1970 ){

    print("You are in your forties.")
    
} else if( nameAndBirthYear.1 <= 1969 && nameAndBirthYear.1 >=  1960 ){

    print("You are in your fifties.")
    
} else if( nameAndBirthYear.1 <= 1959 && nameAndBirthYear.1 >=  1950 ){

    print("You are in your sixties.")
    
} else if( nameAndBirthYear.1 <= 1949 && nameAndBirthYear.1 >=  1940 ){

    print("You are in your seventies.")
    
} else if( nameAndBirthYear.1 <= 1939 && nameAndBirthYear.1 >=  1930 ){

    print("You are in your eighties.")
    
} else if( nameAndBirthYear.1 <= 1929 && nameAndBirthYear.1 >=  1920 ){

    print("You are in your nineties.")
    
} else {

    print("You are at least 100. Good for you!")
    
}


switch nameAndBirthYear{
case (_,2010...2019):
    print("You are between 0 and 9 years of age.")
case (_,2000...2009):
    print("You are between 10 and 19 years of age.")
case (_,1990..1999):
    print("You are in your twenties.") 
case (_,1980..1989):
    print("You are in your thirties.") 
case (_,1970..1979):
    print("You are in your forties.") 
case (_,1960..1969):
    print("You are in your fifties.") 
case (_,1950..1959):
    print("You are in your sixties.") 
case (_,1940..1949):
    print("You are in your seventies.") 
case (_,1930..1939):
    print("You are in your eighties.") 
case (_,1920..1929):
    print("You are in your nineties.") 
default:
    print("You are at least 100. Good for you!")
}


*/
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

/* Question #13 Answer

When teh value of number is 42, the above switch statment will print out, "The answer to life, the universe and everything." 
If the value of number is changed to 365, the switch statement will print out, "Days in year". 
If the value of number is changed to 1024, the switch statment will print out, "Bytes in a Kilobyte." 
If the vaule of number is changed to 65, the switch statement will print out, "Some uninteresting number." 
If you remove the default case, you will run into a compiler error.

*/
***


## Question 14

Consider the variable below called population and the if-condition.

a. Add an else-if-condition that states if population is less than 10000 but greater than 5000, then message changes to say it's "a medium size town".

b. Add an else-condition where message changes to say it's a mid-size town. //WHAT IS THIS ASKING ME TO DO?

c. Convert your final if-else statement to a switch statement.

```swift
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
}
```
/* Question #14 Answer

var population: Int = 10000
var message = String()

if (population > 10000) {

 message = "\(population) is a large town"
 
} else if( population < 100000 && population >= 5000 ){ 

 message = "\(population) is a medium size town."
 
} else {
 
 message = " \(population) is a mid-size town."
 
}

switch population{

case 100000:
message = "\(population) is a large town."

case 5000..<100000:
message = "\(population) is a medium size town."

default:
message = "\(population) is a mid size town."

}

*/
***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional

b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
/* Question #15 Answer
a. 

if ( myTuple.0 + myTuple.1 >= 15){

    print("The sum of the two numbers in the tuple is at least 15.")
    
} else{

    print("The sum of the two numbers in the tuple is less than 15.")
    
}

b.

switch myTuple{
    case (0...,15...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (1...,14...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (2...,13...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (3...,12...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (4...,11...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (5...,10...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (6...,9...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (7...,8...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (8...,7...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (9...,6...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (10...,5...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (11...,4...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (12...,3...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (13...,2...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (14...,1...):
    print("The sum of the two numbers in the tuple is at least 15.")
    case (15...,0...):
    print("The sum of the two numbers in the tuple is at least 15.")
    default:
    print("The sum of the two numbers in the tuple is less than 15.")
}

*/
***
