# Regular Expression (Regex) Tutorial

This tutorial aims to introduce a user into regular expression, often referred to as 'regex', and how to best utilize this tool. 

## Summary

In this tutorial, the goal will be to use regular expression (regex) in order to ensure that an email address entered by a user will be validated to be a real email address. 

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;
```

I will explain how each part of this regex comes into play to accomplish this goal.

## Table of Contents

- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

```js 
var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;
```
In addition, a great resource for testing regex and exploring can be found at https://regex101.com/
## Quantifiers
In Regex, when we use ``` + ```, we are using it to match a string that has the specified characters on the left side followed by one or more items on the right side.

This is used in our example of Regex provided where we use it to match any word character equivalent to ```\w = [a-zA-Z0-9_]``` or ```\.``` matches the character "." one or more times.

Another character we can use in Regex is ``` {} ``` which sets either an exact amount, min and max, or more than one copies of the sequence before the quantifiers.

This is used in our example where ```([a-z\.]{1,3})``` matches the previous token (```[a-z\.]```) between 1 and 3 times, as many times as possible.
## Grouping Constructs
```()``` Captures everything enclosed within the parenthesis. It isolates part of the full match and assignes it an ID to be later referred to within the regex.

## Bracket Expressions
```[]``` Matches a character that is contained within the brackets.

## Character Classes
```\d``` Matches a single character that is a digit.

```\w``` Matches a word character, i.e. [a-zA-Z0-9_].
## The OR Operator
```||``` Is used when we we want to accept character strings and not require it to match all pieces. 
An example of this is here ```^I like (dogs|penguins), but not (lions|tigers).$``` where we will accept dogs OR penguins in the first portion and we will accept lions OR tigers. 
## Flags
When writing Regex the search parameters are delimeted by two slash characters ```/.../``` . At the end i.e. after the second slash character is where we specify theflags.

```g``` (global) It allows for the search to continue after the first match and to continue until no more matches can be found.
## Author
[Tommy Alvarado](https://github.com/tommyalv)
