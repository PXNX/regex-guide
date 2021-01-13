# /regex/

### Components for patterns

#### - Range

    a-z matches an lower case letters from a to z
    0-5 matches any number from 0 to 5

#### [] Match exactly one of the objects inside these brackets

    [a] matches the letter a
    [abc] matches a single letter which can be a, b or c
    [a-z] matches any single lower case letter of the alphabet.

#### () Groups different matches for return purposes
    See examples below.

#### {} Multiplier for repeated copies of pattern defined before it

    [a]{2} matches two consecutive lower case letter a: aa
    [a]{1,3} matches at least one and up to three lower case letter a, aa, aaa

#### + Match at least one, or more, of the pattern defined before it

    a+ will match consecutive a's a, aa, aaa, and so on

#### ? Match zero or one of the pattern defined before it

    Pattern may or may not be present but can only be matched one time.
    [a-z]? matches empty string or any single lower case letter.

#### * Match zero or more of the pattern defined before it

    Wildcard for pattern that may or may not be present.
    [a-z]* matches empty string or string of lower case letters.

#### . Matches any character except newline \n

    a. Matches a two character string starting with a and ending with anything except \n

#### | OR operator

    a|b means either a or b can be matched.
    red|white|orange matches exactly one of the colors.

#### ^ NOT operator

    [^0-9] character can not contain a number
    [^aA] character can not be lower case a or upper case A

#### \ Escapes special character that follows (overrides above behavior)

    \., \\, \(, \?, \$, \^

#### ^ Match must occur at start of string

    ^a First character must be lower case letter a
    ^[0-9] First character must be a number.

#### $ match must occur at end of string

    a$ Last character must be lower case letter a


### Precedence table

order|name|representation
---|---|---
1|parentheses|( )
2|multipliers|? + * {m,n} {m, n}?
3|sequence & anchors|abc ^ $
4|alternation|\|

### Predefined character abbreviations

abbreviation|equal to|meaning
---|---|---
\d|[0-9]|any single digit
\D|[^0-9]|any single character that's not a digit
\w|[a-zA-Z0-9_]|any word character
\W|[^a-zA-Z0-9_]|any non-word character
\s|[ \r\t\n\f]|any space character
\S|[^ \r\t\n\f]|any non-space character
\n|[\n]|new line

### Test it
https://regexr.com/ or https://regex101.com/ work like charm :heart:
