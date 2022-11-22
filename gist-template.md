# Regex Tutotial: Understanding the Components of a Regular Expression

Welcome! 

## Summary

In this tutorial, we will go over the various components of a Regex that is used to validate a matching email as in input by a user. The following Regex we will be looking at is `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Grouping Constructs](#grouping-constructs)
- [Character Set & Bracket Expressions](#character-set-&-bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
Each regex requires anchors. In this regex, the "^" represents the beginning of the string while the "$" represents the end of the string.

### Grouping Constructs
The regular expression that we are looking at is grouped into three different sections, creating a capture group for extrating a substring or using a backreference. These groups are characterized as being grouped within a parenthesis.

In the regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` the three capturing groups are as follows:

* ([a-z0-9_\.-]+)
* ([\da-z\.-]+)
* ([a-z\.]{2,6}) 

Now, let's break down the contents within these capturing groups even further.

### Character Set & Bracket Expressions
The character set is characterized as being grouped within brackets. The email could match any character in the set. Let's dive in to understand all of the character sets in each capture group of our matching email regex. 

([a-z0-9_\.-]+)<br>
* The "a-z" represents a range of characters from "a" to "z" that can be matched in the email.
* The "0-9" represents a range of characters from "0" to "9" that can be matched in the email.
* The "_" represents a match to a  "_" character
* The "-" represents a match to a "-" character

([\da-z\.-]+)<br>
* The "\d" represents a match to any digit character (0-9).

### Quantifiers
([a-z\.]{2,6})<br>
* This character set has a Quantifier. This represents how many instances of a character, group, or character class must be present in the input. In this character set, the quantifier states that there must be a match between 2-6 of the preceding token in the character set.

([a-z0-9_\.-]+)<br>
* The "+" quantifier satates that there must be a match of 1 or more of the preceding token in the character set.

### Character Escapes
To match a character that hs a special meaning in regex, an escape sequence prefix with a backslash must be used. Out regex expression has an escaped character of "\." which represents a match to a "." character.

## Author

Check out my [GitHub Profile](https://github.com/marycv)
