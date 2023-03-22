# Regex Tutorial

this tutorial explains how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does.

## Summary

In this tutorial, I'll explain how to use a regex to match emails, using the expression /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, as an example.

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

#### The characters (^) and ($) are both considered to be anchors.
``` md
The (^) anchor signifies a string that begins with the characters that follow it. This could be in one of two formats:

- An exact string match, such as ^The, where the strings "The" or "The person" match, but "the" and "the person" do not. This is because a regex is case-sensitive.

- A range of possible matches, displayed using bracket expressions. We'll discuss this in the next section.

The ($) anchor signifies a string that ends with the characters that precede it.
```
### Quantifiers

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

For any quesitons, concerns, or modification request contact me at: [Github](https://github.com/RussC22) or [Linkedin](https://www.linkedin.com/in/tavarus-cherry/)

[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
