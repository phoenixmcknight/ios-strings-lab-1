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

var emptyString = " "
for i in 1...10 {
emptyString += String(i)
}
print(emptyString)

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

var emptyString = " "
for i in 5...51 {
if i % 2 == 0 {
emptyString += "\(i) "
}
}
print(emptyString)

***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

var emptyString = " "
var minimumNum = 4
var maxNum = 60
for _ in 1...60 {
if minimumNum < maxNum - 10 {
minimumNum += 10

emptyString += "\(minimumNum) "

}
}


print(emptyString)
***
## Question 4

Print each character in the string `"Hello world!"`

let Hello = "Hello world!"
for letter in Hello {
print(letter)
}

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

var myStringSeven = "Hello world!"
myStringSeven = String((myStringSeven.last)!)
print(myStringSeven)
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

var hello = "hello"

switch hello.count % 2 {
case 0 :
for letter in hello {
print(letter, terminator: "")
}
default :
for (index,letter) in hello.enumerated() {
if index % 2 != 0 {
print(letter)
}
***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

var string1:Character = "a"
string1 == Character("a")

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

var string = "\u{0041}"
var string2 = "A"

string == string2

var string3 = "\u{00C9}"
var string4 = "É"

string3 == string4

var string5 = "æ"
var string6 = "\u{00E6}"

string5 == string6

var string7 = "ß"
var string8 = "\u{00DF}"

string7 == string8

var string9 = "®"
var string10 = "\u{00AE}"

string9 == string10




***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

var HelloWorld = "\u{0048}\u{0065}\u{006C}\u{006C}\u{006F}\u{0020}\u{0020}\u{0077}\u{006F}\u{0072}\u{006C}\u{0064}\u{0021}"
print(HelloWorld)
***
## Question 10

**Using only Unicode**, print out your name.

var FirstNameLastName = "\u{0050}\u{0068}\u{006F}\u{0065}\u{006E}\u{0069}\u{0078} \u{0020}\u{004D}\u{0063}\u{004B}\u{006E}\u{0069}\u{0067}\u{0068}\u{0074}"
print(FirstNameLastName)
***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

var unicodeLang = "\u{004F}\u{006C}\u{00E1}\u{0020}\u{004D}\u{0075}\u{006E}\u{0064}\u{006F}"
print(unicodeLang)
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:\
```
var Flower = "\u{2698}"
let verticalSymbol = "\u{007c}"
let horizontalSymbol = "\u{005f}"
let range11 = 1...11
let range7 = 1...7

for _ in range11 {
print ("\(horizontalSymbol) ", terminator:"")
}
print()
print()


for _ in range7 {

print("\(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol) \(Flower) \(verticalSymbol)")
}
for _ in range11 {
print ("\(horizontalSymbol) ", terminator:"")
}

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
let whitePawn = "\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}\u{2659}"
let white = "\u{2656}\u{2658}\u{2657}\u{2654}\u{2655}\u{2657}\u{2658}\u{2656}"
let black = "\u{265C}\u{265E}\u{265D}\u{265A}\u{265B}\u{265D}\u{265E}\u{265C}"

let blackPawn = "\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}\u{265F}"

let range = 0...7

for  i in whitePawn{
print (i, terminator: " ")
}
print()
for i in white {
print(i, terminator: " ")
}
for _ in 0...3{
print()
}
for  i in blackPawn{
print (i, terminator: " ")
}
print()
for i in black {
print(i, terminator: " ")
}

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```
 var aString = "Replace the letter e with *"
 var replacedString = ""
 
 replacedString += aString.replacingOccurrences(of: "e", with: "*")
 print(replacedString)


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

// Your code here
```
var aString = "this string has 29 characters"
var reverse = ""

for letters in aString {
reverse = "\(letters)" + reverse

}
print(reverse, terminator: "")

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
```
var aString = "racecar"
var reverse = ""

for letters in aString  {
reverse = "\(letters)" + reverse
}
if reverse == aString {
print("true")
} else {
print("false")
}
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
```
var problem = "split this string into words and print them on separate lines"
for words in problem.components(separatedBy: " ")  {

print(words)
}


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
```
var problem = "find the longest word in the problem description"
var split = problem.components(separatedBy: " ")
var max = split.max(by: {$1.count > $0.count})
if max != nil {
print((max)!)
}


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


let sentence = "How are you doing this Monday?"
let wordCount = sentence.filter{ $0.isLetter || $0.isWhitespace }
if let index = wordCount.lastIndex(of: " ") {
let lastWord = wordCount[index...]
print(lastWord.count)
} else {
print("No last word")
}

***
