# Title: Regex tutorial

## Summary
A Regular expression (aka Regex) is a sequence of characters that specifies a search pattern in text. 
In this tutorial, we will see how Regex is used to match an username. 

    /^[a-z0-9_-]{3,16}$/
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
    /^[a-z0-9_-]{3,16}$/
### Anchors
The characters ^ and $ are both considered to be anchors.
The $ anchor signifies a string that ends with the characters that precede it. 
Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.
### Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). 
They frequently include the minimum and maximum number of characters that your regex is looking for.
we have the quantifier {3,16}. This means that we want to find the preceding string pattern a minimum of 3 times and a maximum of 16 times.
### OR Operator
Using the OR operator (|), the expression [abc] could be written as (a|b|c).
Using our example in the grouping constructs section, we can take the original expression:

### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 
### Flags
 Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex.
### Grouping and Capturing
The primary way you group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression.
Grouping constructs have two primary categories: capturing and non-capturing. The details about how capturing and non-capturing groups are used are beyond the scope of this tutorial. 
The important thing to understand is that capturing groups capture the matched character sequences for possible re-use (including a numbered backreference) while non-capturing groups do not.
A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses.
### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match.

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author
https://github.com/oliviakim96/regex-tutorial