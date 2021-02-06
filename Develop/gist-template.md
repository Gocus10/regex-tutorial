# REGEX Email verification

This is a deep dive on the REGEX expression used to validate emails, so that you can understand the pieces of code and what purpose they serve in the expression.

## Summary

> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.
This is the expression used to validate if a string is an email. This expression can be broken down into a few pieces, and these pieces share some similarities. REGEX can be a simple and effective way to do email string validation.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components
Let's look at some of the big pieces first. This expression as a whole mostly contains 3 expressions, Enclosed by brackets []. There are boundaries to determine the start and end of the input. There is an escape with a period, to determine that there must be a period at that point. The + indicates that these components inside of the brackets may occure mulitple times. There are groups(). As well as quantifiers {}.  I'll break down further each of the components in their respective sections below. 
### Anchors
Position anchors notate the start and end of the line or word. We are looking for a line because an email will have multiple words and we are checking the whole of the line. So for that we will notate the start with ^ and the end with $
### Quantifiers
There are quantifiers in this expression. At the end of an email address, you have a set number of characters that are accepted. For instance .com .gov .edu , these are important to determining if the email address is a valid one. This expression limits with quantifiers the number of characters accepted for this string {2,6} between 2 and 6. Where the other 2 brackets with the + symbol will take any number one or more.
### Character Classes
Character classes may be found inside of the brackets in this expression. a-z as well as 0-9. This regex will only accept lowercase letters, numbers, and specifically the characters _\-. for uppercase letters we would need to add A-Z within the brackets. The /d in the second expression is also a character class. it does the same thing as 0-9 refering to any digit.
### Flags
The forward slashes at the beginning and end are also telling something about the start and end. Think of them as quotations for a string. And the period at the end is saying to match one. So match one of everything in these quotations. /blah@blah.blah/ These flags communicate to javascript that everything inside of these is a REGEX.
### Grouping and Capturing
Parentheses group the regex between them. In this expression we can see if we remove the anchors and flags, we have ()@().() which is 3 sets of strings/numbers separated first by an @ symbol then by a . "The period needs a \ infront of it as an escape so that the . is not taken as the regex meaning but instead as just a period"
### Bracket Expressions
Bracket expressions are special character classes. Inside of these brackets characters loose their special powers, so you are able to look for \ d or any character within the brackets as well as ranges like a-z or 0-9.
## Author

Lewis Culbert

[My github](https://github.com/Gocus10)
