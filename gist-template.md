# Regex Tutorial - Match An Email

## Summary

This tutorial will break down each component of a regular expression, or regex, explaining how the following string can be used to match an email:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

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

The characters "^" and "\$" function as anchors to tell the expression where to look for specific characters. The caret anchor "^" points to the beginning of a string, matching the position before the first character. The dollar anchor "\$" matches the position directly following the last character in the string. These help ensure a string will fully match the intended pattern.

### Quantifiers

The quanitfies used in this email regex are "+" and "{2,6}". The plus "+" quanifier refers to one or more characters. Numbers inside curly brackets refer to a specific number of characters. With two numbers separated by a comma, these will be the minimum and maximum number of characters, forming a range. For this example, we have a range from two to six characters specified for the last part of the email address (.com, .net, etc.).

### Grouping Constructs

Subexpressions are grouped using parentheses: ( subexpression ). The subexpressions in this email regex are:

```
([a-z0-9_\.-]+),    ([\da-z\.-]+), and    ([a-z\.]{2,6})
```
The "@" and "." in between are literal characters and will match an "at" symbol and a period.

### Bracket Expressions

A bracket expression is a list of characters, not separated by commas, and enclosed by "[" and "]". It matches any single character in that list, or may contain a range such as a-z or 0-9, separated by a hyphen. If the first character in the list is a caret "^", then the expression matches any character not in the list. The first bracket in this regex will match one or more of any characters including a-z, 0-9, an underscore, period, or hyphen:
```
[a-z0-9_\.-]
```

The next bracket will match one or more of any digit "/d", any letter a-z, a period "\." (escaped with the backslash), or hyphen:
```
[\da-z\.-]
```

The last bracket will match 2-6 characters a-z or a period:

```
[a-z\.]
```

### Character Classes

Certain specific classes of characters are predefined in bracket expressions. None are used in this particular email regex, but some examples for alphanumeric, digits, and blank characters are respectively:
```
[:alnum:]       [:digit:]       [:blank:]
```

### The OR Operator

There are no OR operators being used in this expression, but OR is denoted with the pipe symbol "|".

### Flags

Optional flags can be used to add special functions to regular expressions, such as adding "i" for a case-insensitive search or "g" for a global search.

### Character Escapes

There are certain special characters which must be escaped with a backslash. A couple of examples are the period, as seen in this tutorial's regex, which on its own matches any character. Another example is the asterisk "\*" which means zero or more. Together, ".*" matches everything. A literal parentheses would also need to be escaped, since they are used for grouping.

## Author

Hi! My name is Christina Bohn. I hope this regex tutorial was helpful! I'm currently developing a passion for coding through the University of Washington's Full-Stack Coding Bootcamp. I live with my partner in Tacoma, WA with two cats and a jungle of houseplants. My background is in environmental science, so I am a full-tilt STEM girl and very excited to begin a career in tech!

Here's my Github:

    * https://github.com/ChristinaBohn


Thanks for reading!
