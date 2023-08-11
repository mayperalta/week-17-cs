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

Quantifier + tells our regex to match everything within the Capture group () which in this case is (user email name)@(mailserver)+(domain).

Quantifier {2,6} will allow a match range of 2-6 characters for the character set of [a-z\.].

### Grouping Constructs

Group constructs bind expressions together to evaluate specific information in a specific order.

- Group #1 in this expression is ([a-z0-9_\.-]+) that matches the user email name.
- Group #2 in this expression is ([\da-z\.-]+) that matches the mail server. 
- Group #3 in this expression is ([a-z\.]{2,6}) that matches the domain. 

### Bracket Expressions

Bracket expressions are a list of characters and/or character classes enclosed in brackets [].

There are 3 bracket expressions within the current regex providing sets of character classes.

- Bracket #1 [a-z0-9_\.-] states that it can use any lowercase letter (a-z), any digit (0-9), an underscore, period.
- Bracket #2 [\da-z\.-] states that it can use one or more digits, any lowercase letter (a-z), a period, and a hyphen.
- Bracket #3 [a-z\.] states that it can use any lowercase letter (a-z)

### Character Classes

Character Classes match a character in the input string to any one character set within it.

"a-z" is a lowercase character range
"0-9" is a digit character range
"\d" is one of the “metacharacters” for matching strings
"_" and "-" match their respective characters literally
"." matches a period literally
"@" and the external "." match their respective characters literally at certain positions in the input string

### The OR Operator

The "|" is an OR character that matches any of the characters in the expression. For example, "abc|xyz" returns "abc or xyz". 

### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

### Character Escapes

Whenever you want to match a syntax character literally, you need to escape it with a backslash ( \ ). For example, to match a literal * in a pattern, you need to write \* in the pattern.

## Author

I'm May Peralta, the author of this tutorial document. For more information, view my github at https://github.com/mayperalta/week-17-cs.
