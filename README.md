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
# Answer - this code will print:

## A
## C
## D

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

# Answer
## myCoolApp hasn't released yet

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

# Answer
## D

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
# Answer 
- No parentheses around the conditions
- No opening and closing brackets in each of the cases
## - No default case in the switch statement
- No print statement right outside the switch statement

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```
# Answer
```swift
let currentWeather = "rain"

switch currentWeather {
case "rain":
 print("Get your umbrella!")
case "sunny":
 print("Take your sunglasses!")
case "snow":
 print("Break out your ski gear!")
default:
    print("Typical meteorologist, weather is unknown!")
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

# Answer
```swift
let firstName = "John"
let lastName = "Appleseed"

var fullName: String = firstName + " " + lastName
print("Fellow's full name is \(fullName)")
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
# Answer

```swift
switch temperatureInFahrenheit {
case ..<40:
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
# Answer
```swift
if true {
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

# Answer
```swift
let shape = 4 // let shape = 2

switch shape {
case 3:
     print("This shape is a triangle.")
case 4:
     print("This shape is a square.")
case 5:
    print("This shape is a pentagon.")
case 6:
    print("This shape is a hexagon.")
case 7:
    print("This shape is a heptagon.")
case 8:
    print("This shape is an octagon .")
case 9:
    print("This shape is a enneagon.")
case 10:
    print("This shape is a decagon.")
default:
     print("Error - this shape is unknown.")
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
# Answer 
```swift
let grade = 85

switch grade {
case 100:
     print("A+")
case 90...99:
     print("A")
case 80...89:
    print("B")
case 70...79:
    print("C")
case 65...69:
    print("D")
case ..<65:
    print("F")
default:
     print("Error")
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
# Answer
```swift
let firstName = "Phil"

switch firstName {
case "Peter":
    let lastName = "Gabriel"
    print(firstName + " " + lastName)
case "Phil":
    let lastName = "Collins"
    print(firstName + " " + lastName)
default:
    print("Error")
}
```
***

## Question 12

Write an if statement that prints out what decade of life someone is in (e.g "You are in your twenties). Then, write it as a switch statement.

```swift
let nameAndBirthYear: (String, Int)

```
# Answer
```swift
let nameAndBirthYear = (name: String(), birthYear: Int())
var decadeAge = String()

if nameAndBirthYear.birthYear >= 1990 && nameAndBirthYear.birthYear < 2000  {
    decadeAge = "20's"
} else if nameAndBirthYear.birthYear >= 1980 && nameAndBirthYear.birthYear < 1990 {
    decadeAge = "30's"
} else if nameAndBirthYear.birthYear >= 1970 && nameAndBirthYear.birthYear < 1980 {
    decadeAge = "40's"
} else if nameAndBirthYear.birthYear >= 1960 && nameAndBirthYear.birthYear < 1970 {
    decadeAge = "50's"
} else {
    decadeAge = "Unknown"
}

switch nameAndBirthYear.birthYear {
case 1990...1999:
    decadeAge = "20's"
case 1980...1989:
    decadeAge = "30's"
case 1970...1979:
    decadeAge = "40's"
case 1960...1969:
    decadeAge = "40's"
default:
    decadeAge = "Unknown"
}
print("You're in your \(decadeAge)")
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
# Answer
-a. 365? Prints - Days in year

-b. 1024? Prints - Bytes in Kilobyte

-c. 65? Prints - Some uninteresting number

What happens when you remove the default clause?
Will not compile

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
# Answer 
```swift
var population: Int = 1000
var message = String()

if population > 10000 {
 message = "\(population) is a large town"
} else if population >= 5000 && population <= 10000 {
    message = "\(population) is a medium size town"
} else {
    message = "\(population) is a mid-size town"
}

switch population {
case 10000...:
    message = "\(population) is a large town"
case 5000...10000:
    message = "\(population) is a medium size town"
default:
    message = "\(population) is a mid-size town"
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
# Answer
```swift
let myTuple: (Int, Int) = (5, 10)

let sum = myTuple.0 + myTuple.1

if sum >= 15 {
    print("\(sum) is at least 15")
} else {
    print("\(sum) is less than 15")
}

switch sum {
case 15...:
    print("\(sum) is at least 15")
default:
   print("\(sum) is less than 15")
}
```
***
