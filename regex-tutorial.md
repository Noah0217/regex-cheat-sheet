# Regex Cheat Sheet

A document that allows the user to learn the basics of regex (regular expressions)

## Summary

In this tutorial I will be demonstrating the regex to check for an existing IP address.<br> The regex will look like the following ^(?:[0-9]{1,3}\.){3}[0-9]{1,3}$ Heres an example of an IP address 192.158.1.38

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
Anchors belong to the family of regex tokens that don't match any characters.
- ^(caret) - Matches at the start of the string the regex pattern is applied to.
- $(dollar) - Matches at the end of the string the regex pattern is applied to.

Examples
- `^` matches `^`(?:[0-9]{1,3}\.){3}[0-9]{1,3}$
- `$` matches ^(?:[0-9]{1,3}\.){3}[0-9]{1,3}`$`

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.
- ?(question) - Match zero one or more time.
- {3} - Match exactly 3 times.
- {1,3} - Match from 1 to 3 times.

Examples
- `?` matches ^(`?`:[0-9]{1,3}\.){3}[0-9]{1,3}$ 
- `{3}` matches ^(?:[0-9]{1,3}\.)`{3}`[0-9]{1,3}$
- `{1,3}` matches ^(?:[0-9]`{1,3}`\.){3}[0-9]`{1,3}`$

### Character Classes
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets. If you want to match an a or an e, use [ae]. You could use this in gr[ae]y to match either gray or grey.

Examples
- `\d` - matches any digit from 0-9 ^(?:[`0-9`]{1,3}\.){3}[`0-9`]{1,3}$
- `.` - matches any character ^(?:[0-9]{1,3}\.){3}[0-9]{1,3}$

### Bracket Expressions
A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

Examples
- `[]` - matches ^(?:`[0-9]{1,3}\.){3}[0-9]`{1,3}$

### Greedy and Lazy Match
'Greedy' means match longest possible string. 'Lazy' means match shortest possible string. For example, the greedy h. +l matches 'hell' in 'hello' but the lazy h.

Examples
- `\d+` - matches all possible digits. ^(?:[0-9]{1,3}\.){3}[0-9]{1,3}$
- `?` - matches any character after the quantifier. ^(`?`:[0-9]{1,3}\.){3}[0-9]{1,3}$

## Author

Hi my names Noah Mejia and feel free to check out my other projects.

GitHub Profile - https://github.com/Noah0217

### References
- https://www.regular-expressions.info/refrepeat.html
- https://www.javascripttutorial.net/regular-expression-quantifiers/