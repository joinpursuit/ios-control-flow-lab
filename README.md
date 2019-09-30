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
_________________________________
Answer:
A
C
D
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

________________________________________
Answer:
- myCoolApp hasn't released yet


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
___________________________
Answer:
D

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
_________________________________________________
Answer:
- No default case in the switch statement

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
______________________________
Answer:
let currentWeather = "rain"

switch currentWeather {
case "rain":
print("It's raining today")
case "sun":
print("It's sunny today")
case "snow":
print("It is snowing today")
default:
print("Hope the weather will be great today")
}
```

***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below
__________________________________
Answer:
let firstName = "John"
let lastName = "Appleseed"

var fullName = firstName + " " + lastName

print("Fellow's full name is \(fullName).")

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
_______________________________
Answer:
switch temperatureInFahrenheit {
case 0...40:
    print("It's cold out.")
case 85...150:
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
_____________________
Answer:
let yourScore = 100

if yourScore >= 100 {
 print("You win!")
}
else {
 print("You lose!")
}
// Output "You win!"
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

__________________________
Answer:
Example 1:
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
case 0..<3:
    print("Error")
default:
    print("Error")
}
// Output "Hexagon"

Example 2:
var numberOfSides = 2

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
case 0..<3:
    print("Error")
default:
    print("Error")
}
// Output "Error"
"

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

_____________________________
Answer:
let numericScore = 100

switch numericScore {
case 100...100:
    print("Grade A+")
case 90...99:
    print("Grade A")
case 80...89:
    print("Grade B")
case 70...79:
    print("Grade C")
case 65...69:
    print("Grade D")
case 0..<65:
    print("Grade F")
default:
    print("Error in score calculation")
}
// Output "Grade A+"
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
___________________________________________
Answer:
The second line of code declares a constant (inside the code). That is not acceptable.
There are a lot of ways how to rewrite the code. I would rewrite it like that:

let firstName = "Peter"

if firstName == "Peter" {
 print("Gabriel")
} else if firstName == "Phil" {
  print("Collins")
} else {
    print("Unknown lastname")
}
// Output "Gabriel"

***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
Answer:
let nameAndBirthYear = ("Aaron", 23)

switch nameAndBirthYear {
case ("Aaron", 0...10):
print("Your are a child")
case ("Aaron", 11...20):
print("You are a teenager")
case ("Aaron", 21...30):
print("You are in your twenties")
case ("Aaron", 31...40):
print("You are in your thirties")
case ("Aaron", 41...50):
print("You are in your fourties")
default:
print("You are too old, sorry dude")
}

let nameAndBirthYear = ("Aaron", 23)

if 0...10 ~= nameAndBirthYear.1 {
print("Your are a child")
} else if 11...20 ~= nameAndBirthYear.1 {
print("You are a teenager")
} else if 21...30 ~= nameAndBirthYear.1 {
print("You are in your twenties")
} else if 31...40 ~= nameAndBirthYear.1 {
} else if 41...50 ~= nameAndBirthYear.1 {
print("You are in your fourties")
} else {
print("Ypu are too old too old, sorry dude")
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
 }
```
What happens when you change number to:

-a. 365?

-b. 1024?

-c. 65?

What happens when you remove the default clause?
______________________________________________
Answer:
Currently system will print "The answer to life, the universe and everything".

With let number = 365 will print "Days in year".

With let number = 1024 will print "Bytes in a Kilobyte".

With let number - 65 will print "Some interesting number".

If to remove the default clause we will get error "Switch must be exhaustive"

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
____________________________________________
Answer:
a-b:
var population: Int = 10000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
} else if population > 5000 && population < 10000 {
message = "\(population) is a medium town"
} else {
message = "It's a mid-size town"
}
print(message)

c:
var population: Int = 10000
var message = String()

switch population {
case 10001...:
    message = "\(population) is a large town"
case 5001..<10000:
    message = "\(population) is a medium town"
default:
    message = "It's a mid-size town"
}
print(message)


***

## Question 15

Complete the code below so that it prints out and tells the user if the sum of the two numbers in the tuple is at least 15.

a. Using a conditional

b. Using a switch statement

```swift
let myTuple: (Int, Int) = (5, 10)
```
__________________________________
Answer:
let myTuple: (Int, Int) = (5, 10)
let sumOfMyTuple = myTuple.0 + myTuple.1

if sumOfMyTuple == 15 {
    print("Sum is equal to 15")
} else {
    print("Sum is not equal 15")
}

Using switch:

let myTuple: (Int, Int) = (5, 10)
let sumOfMyTuple = myTuple.0 + myTuple.1

switch sumOfMyTuple {
case 15:
    print("Sum is equal to 15")
default:
    print("Sum is not equal 15")
}
