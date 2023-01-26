# URL Regex Tutorial

## Summary

This document contains a basic understanding of how to read a URL regular expression. I use an example URL that contains all components for the reader to understand. I will break down from outside using the grouping constructors, inside to brackets and how quantifiers affect them in and outside grouping constructs.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)

Matching a URL: `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w\.-]*)*\/?$/`

Example: https://example.com/holy_cow.html

## Regex Components
/ - Start of the regular expression

^ - Anchor Point - starting of URL

(https?:\/\/) - Group #1

? - Quantifier

([\da-z\.-]+) - Group #2 

\. - matches the '.' character

([a-z\.]{2,6}) - Group #3

([\/\w \.-]*) - Group #4

* - Quantifier: Matching 0 or more of the preceding token

\/ - Matching the '/' token

? - Match 0 or more of the preceding token

$ - Anchor Point - Ending of URL

/ - End of the regular expression


### Anchors

 ^ - Signifying the string begins after this character - Where the URL starts
 $ - Signifying the string ends with the character preceding it - Where the URL ends

### Quantifiersdes
? - Match Group #1 expression 0 or 1 time

+ - Match the bracket expression [\da-z\.-] 1 or more times

{2,6} - Match the bracket expression [a-z\.] minimum 2 times but at a maximum of 6

* - Match the bracket expression [\/\w \.-] 0 or more times

* - Match the group expression ([\/\w \.-]*) 0 or more times


### Grouping Constructs
(https?:\/\/) - Capturing group #1: capturing group looking for https:// 

([\da-z\.-]+) - Capturing group #2: \d matches any digit, a-z matching any lower case letter, \. matches the '.', - matches the '-' character. This will give you the 'www.example' after the https:// so in total we https://www.example

([a-z\.]{2,6}) - Capturing group #3: This gives you the domain extension we're used to seeing, like .com or .org -> in total we have https://www.example.com

([\/\w \.-]*) - Capturing group #4: The \/ gives us the / for starting the route path, the \w matches any alphanumeric character and _ as well, along with \. giving you the '.' and the - gives the '-' character. This will give you final routing of holy_cow.html -> https://www.example.com/holy_cow.html is now valid

### Bracket Expressions
[\da-z\.-]
\d -> match any digit 0-9
a-z -> match any lowercase letter
\. -> gives you the '.' like .com\
- -> gives you the '-'

[a-z\.]
a-z -> match any lowercase letter
\. -> gives the '.' like .com

### Character Classes
a-z -> matches for lower case letter a-z

### Character Escapes
\. -> escapes for '.'
\/ -> escapes for '/'

## Author

My name is Matthew Gaskins and I'm currently enrolled in the UofU 24 week coding bootcamp. I have a BS in Mechanical Engineering from the University of Houston with a minor in Mathematics. I'm using this opportunity to learn a different set of skills to compliment the ones I've developed through college and working. I'm hoping to get a remote position which will allow my work location to flexible as my wife is in medical school and can be moving a few times in the next 5-10 years. I've linked my github repository down below.

https://github.com/mgaskins17

