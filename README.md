# RegEx-Tutorial
A tutorial that explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.

## Table of Contents

- [Summary](#summary)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)

## Summary
This is one type of regex used for email validation:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Lets break down the components of this patter to see how each part is used to match the pattern of an email.

## The Components

### Anchors
Anchors are a type of token that are unique by defining something in the string or the process of matching by matching the current position of the engine in the string to match a determined location. 

In the instance of `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the anchors are `^` and `$`.

The carrot marks the begining of a string and question mark signals the end of a string although there is variation of what they do depending on the coding language they are used in so double check before using them.

### Quantifiers
Quantifiers are define the number of characters that can be used but different languages define quantifiers differently but for RegEx this is the definition.

In the instance of `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the quantifiers are  in `([a-z\.]{2,6})$/` where it determine the pattern for the ending of email as .com, .net, .edu or any other possible ending that had the letters a-z and the number of characters from 2-6 at the end of the email.

### OR Operator
This component goes by multiple names but it is just the `|` and though this RegEx doesn't contain any it could be used to search for only two specific types of email ending making those endings the only acceptable inputs for email.

Example.
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.(com|net)$/`

### Character Classes
Character classes are straight foward as they define the types of characters that can be used such as letters, numbers, symbols, and more. The character you want to match are placed inside `[]` and `-` inbetween can show the range of characters that can be used

In `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the character classes are a-z, and 0-9

### Flags
In RegEx this is an optional step and there are 6 types:

 `/i ignore casing` 
 `/g global searching`
 `/s single line`
 `/m multi line`
 `/y sticky search`
 `/u unicode`

 ### Bracket Expression
 Bracket expressions are used to determine parameters. In this RegEx it is used to determine the range of letters and numbers.
