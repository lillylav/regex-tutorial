# Regex Tutorial

In this tutorial I'm going to be walking through a regular expression(regex) which is a series of characters meant to help a programmer search a dataset for a string which is formatted in a particular way. This is useful for email addresses, phone numbers, regular addresses, and more.

## Summary

The specific regex I'm going to describe is one to validate email addresses:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Bracket Expressions](#bracket-expressions)


## Regex Components

### Anchors
This expression uses '^' at the beginning of the expression and '$' at the end of the expression to define the expression's boundaries.

### Quantifiers
This expression uses the '+' quantifier in the first 2 sections (the section before the '@' and the section after the '@' but before the '.'). The '+' quantifier comes after the defined character set and allows for one or more (with no limit) of the defined characters to be present. The final section uses the '{2,6}' quantifier which defines that section as being between 2 and 5 characters in length.

### Character Classes
This expression uses the '/d' character class which matches a single character that is a digit.

### Flags
The '/' at the beginning and end of the expression are flags, these note the beginning and end of the regex expression.

### Bracket Expressions
For an email address there are multiple character sets defined in bracket expressions: 
- The first character set defined is the characters that comes before the '@' symbol. It is defined as '[a-z0-9_\.-]' in the regex, this character set matches lowercase letters a-z, numbers 0-9, and '_', literal '.', and '-' special characters.
- The second character set defined is for the section of the email address that comes after the '@' but before the period. It is defined as '[\da-z\.-]' in the regex, this character set matches a single character that's a digit, letters a-z, and '-' and literal '.' special characters.
- The third and final character set is the set of characters that comes after the period. It is defined as '[a-z\.]' in the regex, this character set matches lowercase letters a-z and the literal '.' special character.

## Author
Written by Lilly Leiran a full stack web developer who writes in HTML, CSS, and JavaScript with knowledge of MySQL and Node.js
#### Github: https://github.com/lillylav