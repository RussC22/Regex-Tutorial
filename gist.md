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

```md
The (^) anchor signifies a string that begins with the characters that follow it. This could be in one of two formats:

- An exact string match, such as ^The, where the strings "The" or "The person" match, but "the" and "the person" do not. This is because a regex is case-sensitive.

- A range of possible matches, displayed using bracket expressions. We'll discuss this in the next section.

The ($) anchor signifies a string that ends with the characters that precede it.
```

### Quantifiers

```
Quantifiers specifies how many instances of the previous element must be present in the input string for a match to occur;
in this pattern, the quantifiers are used to match a specific number of occurrences of a character or group of characters. The following quantifiers are used in this regex pattern:

+ - Matches one or more occurrences of the preceding character or group. For example, [a-z0-9_.-]+ matches one or more occurrences of any lowercase letter, digit, underscore, period, or hyphen.

* - Matches zero or more occurrences of the preceding character or group. For example, [\da-z.-]* matches zero or more occurrences of any digit, lowercase letter, period, or hyphen.

{2,6} - Matches between 2 and 6 occurrences of the preceding character or group. For example, [a-z.]{2,6} matches between 2 and 6 occurrences of any lowercase letter or period.
```

### Grouping Constructs

```
Grouping constructs in this regex pattern help to define the structure of a valid email address and allow you to extract specific parts of the email address using capture groups. The grouping constructs are represented by the parentheses () and they serve two main purposes:

To capture the matched substrings: The parts of the pattern that are enclosed in parentheses are called capture groups, and they allow you to extract specific parts of the matched string. In this particular regex pattern, there are three capture groups:
- The first capture group ([a-z0-9_.-]+) captures the username part of the email address.

- The second capture group ([\da-z.-]+) captures the domain name part of the email address before the dot (.).

- The third capture group ([a-z.]{2,6}) captures the top-level domain (TLD) part of the email address after the dot (.).

To group together subpatterns: Grouping constructs can also be used to group together subpatterns within a larger pattern, which can be useful for applying quantifiers or alternations to specific parts of the pattern.
For example, in the regex pattern ([\da-z.-]+)\.([a-z.]{2,6}), the grouping construct ([\da-z.-]+) groups together the characters that can appear in the domain name part of the email address, and the dot (\.) outside the grouping construct matches the dot that separates the domain name from the TLD.
```

### Bracket Expressions

```
There three sets of parentheses to capture groups of characters; the three groups contains three bracket expressions for each of the three groups:

- [a-z0-9_.-]+
  This group matches one or more characters that are either lowercase letters, digits, underscores, dots, or hyphens.

- [\da-z.-]+
  This group matches one or more characters that are either digits, lowercase letters, dots, or hyphens.

- [a-z.]{2,6}
  This group matches between 2 and 6 characters that are either lowercase letters or dots.
Character Classes
```

### Character Classes

```
Character classes match specific types of characters in the expression; these are the character classes used:

- [a-z0-9_.-]
  This character class matches any lowercase letter, digit, underscore, dot, or hyphen.

- [\d]
  This character class matches any digit from 0 to 9.

- [a-z]
  This character class matches any lowercase letter from a to z.

- [.]
  This character class matches a literal dot character.
```

### The OR Operator

```
The OR operator in regular expressions is denoted by the pipe symbol '|' and allows for matching one pattern or another. However, the regular expression ^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$ does not use the OR operator. Instead, it uses character classes and specific patterns to match certain types of characters in the email address.
```

### Flags

```
Flags are optional parameters that modify the behavior of the expression; they are added after the closing delimiter of the regular expression and can change the way that the expression is matched, such as ignoring case or matching across multiple lines.

- ^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$ does not use any flags.
```

### Character Escapes

```
a backslash is used to escape a character that has a special meaning in the regular expression syntax, so that it is treated as a literal character to be matched; ^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$ uses several character escapes to match specific characters. Here are the character escapes used in this regular expression:

- \d
  This character escape matches any digit from 0 to 9. It is used inside the second group to match a digit.

- \.
  This character escape matches a literal dot character. It is used to match the dot that separates the domain name.
For any quesitons, concerns, or modification request contact me at: Github or Linkedin

GitHub license
```

## Author

For any quesitons, concerns, or modification request contact me at: [Github](https://github.com/RussC22) or [Linkedin](https://www.linkedin.com/in/tavarus-cherry/)

[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
