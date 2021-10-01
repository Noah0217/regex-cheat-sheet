# Regex Cheat Sheet

A document that allows the user to learn the basics of regex (regular expressions)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors belong to the family of regex tokens that don't match any characters.
- ^(caret) - Matches at the start of the string the regex pattern is applied to.
- $(dollar) - Matches at the end of the string the regex pattern is applied to.

Examples
- `^` matches `a` in abc/ndef
- `$` matches `f` in abc/ndef

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.
- *(asterisk) - Matches zero or more times
- +(plus) - Matches one or more times
- ?(question) - Match zero one or more time.
- {n} - Match exactly n times.
- {n,} - Match at least n times.
- {n,m} - Match from n to m times.

Examples
- `*` matches `def` ghi in abc def ghi jkl
- `+` matches `def` ghi in abc def ghi jkl
- abc`?` matches `abc` or `ab`
- `a{3}` matches `aaa`
- `a{2,}` matches `aaaaa` in aaaaa
- `a{2,4}` matches `aaaa` `aaa` or `aa`

### OR Operator
Alternatives match one of a choice of regular expressions: if you put the character(s) representing the alternation operator between any two regular expressions a and b , the<br> result matches the union of the strings that a and b match.
- |(bar) - Matches the union of the strings that a and b match.
- [](bracket) - The regex [a-z] will match any letter a through z.

Examples
- `|` matches `(t|T)` to t ot T
- `[]` matches `abc` in a, b , or c

### Character Classes
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets. If you want to match an a or an e, use [ae]. You could use this in gr[ae]y to match either gray or grey.
- \d - matches any digit from 0-9
- \D - matches any non-digit 
- \s - matches any whitespace character (spaces, tabs, etc)
- \S - matches all but \s
- \w - matches any character from a-z
- \W - matches all but \w
- . - matches any character

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

### References
- https://www.regular-expressions.info/refrepeat.html
- https://www.javascripttutorial.net/regular-expression-quantifiers/