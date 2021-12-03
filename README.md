# Regex Tutorial - Matching an Email

Explains the regular expression used for email filtering: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Summary

When using Regex, or regualar expressions, these what can appear to be random symbols strung together actual represent the structure
of a search pattern. This can be used to find multiple strings of information that say different things but follow the same
pattern. This can be used to validated inforation, search documents, and to replace or update information. In this particular
instance this tutorial will touch on regex in an email.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
 - ^ signals the beginning of a string
 - $ signals the end of the string 

### Quantifiers
 - in this example {2,6} quantifies the amount of characters to expect in the particular block of the search it is inserted into
 - the minimum of characters being 2 and the maximum being 6. To under or over shoot these two numbers would filter out certain strings.
 In this case {2,6} is allowing for .com to show in the email search pattern. 

### OR Operator
 - "+" connects different search patterns together. This will connect together the email name + email service + .com

### Character Classes
- \d matches any single character between 0-9

### Flags
- are optional expressions that you can include to make the regex search in a different way. This is included by using single letters
that each search for a different modification that can occur in a regular expression. In this email example no flags are used.

### Grouping and Capturing
- using () you can group together certain expressions and define what type of string or data pattern will show in that group. 
- There are three used in this expression:
    - ([a-z0-9_\.-]+)
    - ([\da-z\.-]+)
    - ([a-z\.]{2,6})

### Bracket Expressions
- Inside of brackets include the parameters of the search patters you are looking for withing each group. 
    - ([a-z0-9_\.-]+) matches any lowercase letter between a-z, any number between 0-9, and any of these listed symbols: "_\.-]"
    - ([\da-z\.-]+) does the same thing as the previous bracket expression but instead of using 0-9 you can shorthand \d
    - ([a-z\.]{2,6}) matches any lowercase letters and the character "." and also only allows 2-6 characters to come after the "."

### Greedy and Lazy Match
- greedy matches will try to match to as many combinations of the search patteren return, depending on documentation, the most results.
Since this has the + sign in it the regex will match as many times as possible. 

## Author

Kaylee Stevens AKA Kayls. Graphic desinger by day, bootcamp goer by night, soon to be a full stack developer. 
https://github.com/kayldubs
