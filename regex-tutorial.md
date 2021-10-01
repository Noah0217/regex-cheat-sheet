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

Examples
- `\d` - matches any digit from `0-9`
- `\D` - matches any non-digit 
- `\s` - matches any whitespace character (spaces, tabs, etc)
- `\S` - matches all but `\s`
- `\w` - matches any character from `a-z`
- `\W` - matches all but `\w`
- `.` - matches any character

### Flags
By default, the dot character in a regular expression matches everything, but newline characters. To get it to match newline characters as well, we are given the s flag.

Examples
- `i` - With this flag the search is case-insensitive: no difference between A and a
- `g` - With this flag the search looks for all matches, without it – only the first match is returned.
- `m` - Multiline mode (covered in the chapter Multiline mode of anchors ^ $, flag "m").
- `s` - Enables “dotall” mode, that allows a dot . to match newline character \n.
- `u` - Enables full Unicode support. The flag enables correct processing of surrogate pairs.
- `y` - “Sticky” searching at the exact position in the text/

### Grouping and Capturing
Capturing groups are a way to treat multiple characters as a single unit. They are created by placing the characters to be grouped inside a set of parentheses. For example, the regular expression (dog) creates a single group containing the letters "d", "o", and "g".

Examples
- `()` - `(abc){3}` matches `abcabcabc` first group matches `abc`.
- `(?:x)` -  Matches `x` but does not remember the match.
- `x|y` - Matches either `x` or `y`.

### Bracket Expressions
A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

Examples
- `[]` - matches `abc` in a, b, or c
- `[^]` - matches `a-z`
- `[[::]]` - matches any character `a-z`

### Greedy and Lazy Match
'Greedy' means match longest possible string. 'Lazy' means match shortest possible string. For example, the greedy h. +l matches 'hell' in 'hello' but the lazy h.

Examples
- `\d+` - matches all possible digits.
- `?` - matches any character after the quantifier.

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)

### References
- https://www.regular-expressions.info/refrepeat.html
- https://www.javascripttutorial.net/regular-expression-quantifiers/