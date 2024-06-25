# Regex Tutorial : Matching a URL

The **regular expression**, also known as **regex** is a sequence of characters that forms a search pattern. It is primarily used for string matching, searching, and manipulation. Regular expressions are powerful tools in programming and text processing, allowing for complex pattern matching and text manipulation.  
In this tutorial, you will learn about **matching a URL**.

## Summary

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`  
The above given pattern is the regex expression for searching the correct URL. This is used to validate against the verified URL pattern.

## Table of Contents

-   [Anchors](#anchors)
-   [Quantifiers](#quantifiers)
-   [Grouping Constructs](#grouping-constructs)
-   [Bracket Expressions](#bracket-expressions)
-   [Character Classes](#character-classes)
-   [The OR Operator](#the-or-operator)
-   [Flags](#flags)
-   [Character Escapes](#character-escapes)

## Regex Components

### Anchors

The characters `^` and `$` are the anchors of the regex.  
The `^` specifies the start of the regex. If is is `^Hello`, the string should start with `Hello`. It is case sensitive and must be in exact way, not even `hello`.  
The `$` gives the end of the regex. It follows the same rules as the start. Anything before it must be same and case-sensitive.

### Quantifiers

The **Quantifiers** in regex specify how many times an element (character, group, or character class) must occur to match.

-   `*`: To specify zero or more times
-   `+`: To specify one or more times
-   `?`: To specify zero or one time
-   `{}`: Curly brackets can provide three different ways to set limits for a match:
    -   `{ n }`: To specify exactly n number of times
    -   `{ n, }`: To specify at least n number of times
    -   `{ n, x }`: To specify from a minimum of n number of times to a maximum of x number of times

URL expression contains `{2,6}`, which specifies the patterb before it must contains atleast `2` and maximum `6` characters

### Grouping Constructs

### Bracket Expressions

The **Bracket Expression** also known as the **positive character classes** as they specifies the characteres we want to include:

-   `[\da-z\.-]`: This character class matches any digit (\d), lowercase letter (a-z), dot (.), or hyphen (-).
-   `[a-z\.]`: This character class matches any lowercase letter (a-z) or dot (.).
-   `[\/\w\.-]`: This character class matches any slash (\/), word character (\w which includes letters, digits, and underscores), dot (.), or hyphen (-).

### Character Classes

### The OR Operator

### Flags

### Character Escapes

**Escape characters** in regex are used to give special meaning to characters that would otherwise be treated as literals or to escape characters that have a special meaning in regex syntax. The escape character in regex is the backslash `\`.

-   `\:`: specifies the `:`
-   `\/`: specifies the `/`
-   `\.`: specifies the `.`

It's important to note that all special characters, including the backslash (\), lose their special significance inside bracket expressions.

## Author

© Udit Sachdeva, `https://github.com/usachdeva`
