# Title: Regex tutorial - Email Address Validation

## Summary
A Regular expression (aka Regex) is a sequence of characters that specifies a search pattern in text. 
In this tutorial, we will see how Regex is used to match email addresses. 

    
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
    /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
### Anchors
The characters ^ and $ are both considered to be anchors.
The ^ anchor signifies a string that begins and $ anchor signifies a string that ends with the characters that precede it. 
Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.
### Quantifiers
Quantifiers set the limits of the string that your regex matches (or an individual section of the string). 
They frequently include the minimum and maximum number of characters that your regex is looking for.
Quantifiers in this regex includes the + operator, which will connect the users email name + email service + .com.
### OR Operator
Using the OR operator (|), the expression [abc] could be written as (a|b|c).
But, there is no Or Operator in the example component.                    
               
### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. 
The character class in this expression is \d, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44".

### Flags
Flags are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex. Regular expressions may have flags that affect the search.
There are only 6 of them in JavaScript: i,g,m,s,u,y
But, there is no flag in the example component. 
### Grouping and Capturing
The primary way you group a section of a regex is by using parentheses (()). Each section within parentheses is known as a subexpression.
Grouping constructs have two primary categories: capturing and non-capturing. The details about how capturing and non-capturing groups are used are beyond the scope of this tutorial. 
The important thing to understand is that capturing groups capture the matched character sequences for possible re-use (including a numbered backreference) while non-capturing groups do not.
A grouping construct can be made non-capturing by adding the characters ?: at the beginning of an expression inside the parentheses
Capturing group #1 in this expression is ([a-z0-9_\.-]+) that matches the user email name. The second capturing group is ([\da-z\.-]+) which will match the email service. Then lastly, capture group #3 is ([a-z\.]{2,6}) to capture the .com.
### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match.
Bracked expressios for email validation includes the character sets of [a-z0-9_\.-], which is matching any letter a-z and is case senstive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; [\da-z\.-], which is matching a single digit from 0-9, any character a-z (case senstive), and the characters "." and "-".; [a-z\.] matches any character a-z(case senstive) and the character ".".
### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the + Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is {} when matching `{2,6} for the last capture group.
### Boundaries
A word boundary, in most regex dialects, is a position between \w and \W (non-word char), or at the beginning or end of a string if it begins or ends (respectively) with a word character ( [0-9A-Za-z_] ).
### Back-references

A backreference in a regular expression identifies a previously matched group and looks for exactly the same text again.
### Look-ahead and Look-behind
Lookahead allows to add a condition for “what follows”.

Lookbehind is similar, but it looks behind. That is, it allows to match a pattern only if there’s something before it.
## Author
https://github.com/oliviakim96/regex-tutorial