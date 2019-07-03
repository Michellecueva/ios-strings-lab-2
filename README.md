# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code

var problem = "split this string into words and print them on separate lines"

for word in problem.components(separatedBy: " ") {
    print(word)
}
```

Example

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


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "

var condensedString = testString.replacingOccurrences(of: "[ ]+", with: " ", options: .regularExpression)

print(condensedString)

```


## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

``` swift
var sampleInput = "Swift is the best language"

var arr = sampleInput.components(separatedBy: " ")

for word in arr.reversed() {
    print(word, terminator: " ")
}


```


## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

``` swift

var sampleInput = "danaerys dad cat civic bottle"

var arr = sampleInput.components(separatedBy: " ")
var count = 0

for word in arr() {
if String(word) == String(word.reversed()){
count += 1
}

}

print(count)

```


## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`
``` swift

var input = "PPALLP"
var aCount = 0
var lCount = 0

for char in input {
    if char == "A" {
        aCount += 1
    }
}

if input.contains("LLL") {
    lCount += 1
}


if aCount > 1 || lCount > 0{
    print(false)
} else {
    print(true)
}


```

## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`
