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

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

© Udit Sachdeva, `https://github.com/usachdeva`
