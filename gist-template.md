# Match an Email - Regex Tutorial

This tutorial is going to explain the use of regex to match emails using the expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. 

## Summary

Regular expression defines a pattern of characters which is used for pattern-matching in “search-and-replace” text functions. It allows to create patterns that help match, locate, and manage text a string of characters like used in an e-mail address or password to produce actionable information.

This tutorial will walk-through the components of a regex and how it applies to matching an email.


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

Anchors provide a way to limit how a regex matches a particular string by telling the regex engine where matches can begin and where they can end.

The anchors used in this regex expression are ^ or caret which indicates the beginning of a string or the beginning of a line if the multiline flat (m) is enabled, and $ to indicate the end of the string. 

### Quantifiers

Quantifiers match a number of instances of a character, group, or character class in a string. They also determine whether a regex will attempt a Greedy match or a Lazy match.

There are two quantifiers in this regex, the + character and (2) a range of {2,6}.

Quantifier + tells our regex to match everything within the Capture group () which is (user email name)@(mailserver)+(domain).

Quantifier {2,6} will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping Constructs

Group constructs bind expressions together to evaluate specific information in a specific order.

- Group #1 in this expression is ([a-z0-9_\.-]+) that matches the user email name.
- Group #2 in this expression is ([\da-z\.-]+) that matches the mail server. 
- Group #3 in this expression is ([a-z\.]{2,6}) that matches the domain. 

### Bracket Expressions

### Character Classes

Character Classes match a character in the input string to any one character set within it.

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
