# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

```swift
var numberString = (1...10)

for x in numberString {
print(String(x), terminator: " ")
}
```

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

```swift
var numberString = (5...51)

for x in numberString {
if x % 2 == 0 {
print(String(x), terminator: " ")
}
}
```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```swift
var numberString = (1...60)
var starter = 4

for _ in numberString {
if starter <= 60 {
print(String(starter), terminator: " ")
starter += 10
}
}
```

***
## Question 4

Print each character in the string `"Hello world!"`

```swift
var string = "Hello world!"

for character in string {
print(character)
}

```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

```swift
let myStringSeven = "Hello world!"

print(myStringSeven.last ?? 12)

```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```swift

```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

```swift
let firstCanCombo = "\u{0075}\u{0308}"
let firstCanSingle = "\u{00FC}"
print(firstCanCombo == firstCanSingle)

let secondCanCombo = "\u{0075}\u{0302}"
let secondCanSingle = "\u{00FB}"
print(secondCanCombo == secondCanSingle)

let thirdCanCombo = "\u{0075}\u{0301}"
let thirdCanSingle = "\u{00FA}"
print(thirdCanCombo == thirdCanSingle)

let fourthCanCombo = "\u{0075}\u{0300}"
let fourthCanSingle = ("\u{00F9}")
print(fourthCanCombo == fourthCanSingle)

let fifthCanCombo = "\u{0079}\u{0301}"
let fifthCanSingle = ("\u{00FD}")
print(fifthCanCombo == fifthCanSingle)
```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

```swift
print("\u{0048}\u{0045}\u{004C}\u{004C}\u{004F}\u{00A0}\u{0057}\u{004F}\u{0052}\u{004C}\u{0044}\u{0021}")
```
***
## Question 10

**Using only Unicode**, print out your name.

```swift
print("\u{004C}\u{0069}\u{0061}\u{006E}\u{0061}")
```
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

```swift
print("\u{00A1}\u{0048}\u{004F}\u{004C}\u{0041}\u{00A0}\u{004D}\u{0055}\u{004E}\u{0044}\u{004F}\u{00A1}")
```
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -

var dashes = "\u{02D7} "
var flower = "\u{2698}"
var horizontalDash = "\u{007C}"

let topAndBottom = String(repeating: dashes , count: 11)
print(topAndBottom)

for _ in 1...7 {
for _ in 1...5 {
print("\(horizontalDash) \(flower) ", terminator: "")
}
print(horizontalDash)
}
print(topAndBottom)
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
//Your code here
let replacedString = aString.replacingOccurrences(of: "e", with: "*")
print(replacedString)

 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

//Your code here
var aString = "this string has 29 characters"
var reverse = String(aString.reversed())
print(reverse)

```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here
let aString = "anutforajaroftuna"
let aStringBackwards = String(aString.reversed())
print(aString == aStringBackwards)
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
var problem = "split this string into words and print them on separate lines"

for character in problem {
if character == " " {
print()
continue
}
print(character, terminator: "")
}
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
var problem = "find the longest word in the problem description"
var compOfProblem = problem.components(separatedBy: " ")
var compHolder = ""

for comp in compOfProblem {
if comp.count > compHolder.count {
compHolder = comp
}
}
print(compHolder)
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***
