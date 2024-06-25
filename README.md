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

**Grouping constructs** in regular expressions are used to treat multiple characters as a single unit. They are enclosed within parentheses `()` and serve several purposes, including capturing matched substrings, applying quantifiers to entire groups, and establishing precedence for alternation `|` operators.

-   `^(https?:\/\/)?`:
    -   This group is optional (? quantifier at the end) and captures the protocol part of the URL (http://, https://, or none).

*   `([\da-z\.-]+)\.`:
    -   Captures the domain name part of the URL, including alphanumeric characters (\d and [a-z]), dots (.), and hyphens (-), ending with a literal dot (.).
*   `([a-z\.]{2,6})`:
    -   Captures the top-level domain (TLD) part of the URL, ensuring it consists of lowercase letters ([a-z]) and dots (.), with a length between 2 and 6 characters.
*   `([\/\w \.-]_)_`:

    -   Captures the path part of the URL, including slashes (\/), word characters (\w), spaces ( ), dots (.), and hyphens (-). The asterisk (\*) quantifier means it can match zero or more occurrences.

*   `\/?$`:
    -   Matches an optional trailing slash (\/?), ensuring flexibility at the end of the URL.

### Bracket Expressions

The **Bracket Expression** also known as the **positive character classes** as they specifies the characteres we want to include:

-   `[\da-z\.-]`: This character class matches any digit (\d), lowercase letter (a-z), dot (.), or hyphen (-).
-   `[a-z\.]`: This character class matches any lowercase letter (a-z) or dot (.).
-   `[\/\w\.-]`: This character class matches any slash (\/), word character (\w which includes letters, digits, and underscores), dot (.), or hyphen (-).

### Character Classes

A **character class** in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. The **bracket expressions** are considered character classes. There are several character classes `[]` are used to define sets of characters that the regex engine will match against.

-   `.`: Matches any character except the newline character (\n).

*   `\d`: Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

-   `\w`: Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

-   `\s`: Matches a single whitespace character, including tabs and line breaks

### The OR Operator

In regex, the **OR** operator allows you to specify multiple alternative patterns to match. It is used as `|`.

### Flags

In regex, **flags** modify the behavior of the regex pattern matching. They are typically used as additional parameters when compiling or executing a regex pattern to control how the matching process works. However, in many regex implementations, flags are not directly embedded in the regex pattern itself but are instead passed as arguments to functions like re.compile() or re.match().  
The above URL regex pattern is well-formed for matching URLs and doesn't require any flags for its intended functionality.

### Character Escapes

**Escape characters** in regex are used to give special meaning to characters that would otherwise be treated as literals or to escape characters that have a special meaning in regex syntax. The escape character in regex is the backslash `\`.

-   `\:`: specifies the `:`
-   `\/`: specifies the `/`
-   `\.`: specifies the `.`

It's important to note that all special characters, including the backslash (\), lose their special significance inside bracket expressions.

## Author

© Udit Sachdeva, `https://github.com/usachdeva`
