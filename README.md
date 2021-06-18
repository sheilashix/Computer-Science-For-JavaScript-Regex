# Computer-Science-For-JavaScript-Regex
# REGULAR EXPRESSION(REGEX)

Regular expression is a sequence of characters that defines a search pattern 
for texts. It acts as a function in that it you specify a sequence of instructions in an imperative
programming language and returns a result or even may cause a side effects.


## Summary
Regex is an expression detailing the search pattern of texts. It is quite wide and also has rules on how they
should be defined and used.I am going to be describing anchors used to match characters, quantifiers used to quantify how many times an expression should be repeated,OR operator used to match choices, Character classes used to match specific characters, flags which are added to expressions to make it search in a different way,grouping and capturing  which is a way of finding data with similar characteristics,bracket expressions which is an expression enclosed in square brackets, greedy and lazy match which is a way to  match the longest or the shortest possible string,boundaries which marks the beginning or end of a script,back-reference which is the previous part of a matched regular expression and finnaly look-ahead and look-behind which matches the character then gives up the result and returns only the match.
```
This is an example of a regex used to match an IP address
/^(?:(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(?:25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$/

```
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
Regex is made up of literals and meta characters. A literal is a single character in a regex line. 
A meta character comprises of several units that have a meaning. The main components of a literal are:
character classes, quantifiers and position variables.
### Anchors
It is used to match a character before, after or a position between characters.
They include:``` ^,$,-.```
```
^Host  matches any string that starts with Host.
lend$  matches any string that ends with lend
^Lend to host$ exact string match.
post matches any string that has post in it.

```
### Quantifiers
Quantifiers are used to quantify how many times a part of an expression should be repeated.
If  you want a something to be repeated in a regex expresion, you write a quantifier after it to specify
how many times it should be repeated.
They include: ```?,+,*,{N},{N,M},{N,}{,N}```
```
list* matches a string that has lis followed by 0 or more t
list+ matches a string that has lis followed by one or more t
list? matches a string that has lis followed by zero or one t
list{2} matches a string that has lis followed by 2 t
list{2,} matches  a string that has lis followed by 2 or more c
list{2,6} matches a string that has lis followed by 2 up to 6 t
li(st)* matches a string that has li followed by zero or more copies 
of the sequence st
li(st){2,6} matches a string that has li followed by 2 up to 6 copies of
the sequence st

```

### OR Operator
The OR operator is used to match one of a choice of regular expressions.
It includes:``` | or []```
```
w(x|y) matches a string that has w followed by x or y
w[xy]  matches a string that has w followed by x or y but without capturing either.
```

### Character Classes
It is used to tell the regex engine to match only one out of several characters.
it includes:```\d\w\s and . ```
```
\d matches a single character that is  a digit
\w matches a word character
\s matches a whitespace character
. matches any character
``` 
### Flags
Flags are optional parameters that we can add to a plain expression to make it search in a different way.
it includes:```i,g,m ```
```
/Hello/i makes the expression case insensitive
m when enabled ``^`` and ``$`` will match the start and end of string
g does not return after the first match
```

### Grouping and Capturing
Grouping and capturing is a way to get a result of matches from a group of digits,characters or
list with similar characteristics using regex expressions, but without knowing or describing much detail about
them.
```
/^[a-z0-9_-]{6,18}$/ this is used to match passwords.
/^[a-z0-9-]+$/  this is used to match a slug

```
### Bracket Expressions
Bracket expression consists of an expression enclosed in square brackets that shall match a specific set
of characters or a specific set of multi character elements based on non empty set of list expressions contained in the bracket expression.
```
[0-9] matches to numbers between 0 to 9 .
[a-zA-Z] matches both upper and lower case letters between a to z

```

### Greedy and Lazy Match
Greedy matching will consume as much as possible or try to match the longest possible string.
lazy matching will consume much less or try to match the lowest possible string.
```
w.+1 matches "wind" in "window"
w.+?1 matches "win" in "window"

```

### Boundaries
A boundary is  a position between \w and \w or simply the beginning or end of a script if it ends or
begins with a word character.
A boundary can occur when: the first character is a word character.
                          after the last character in the string.
                          between two characters in a string.
```
(?(?<=\w) (?!\w)  | (?!\W)  ) used to identify a word boundary
```
### Back-references
Back-references are regular expression commands which refer to a previous part of the matched regular expression. That is they are used to match the same content as previously matched.
```
/^(.)(.)(.)\3\2\1$/p  first 3 letters are subexpressions followed by three back references. it 
is used to search for 6 letter palindrome.

```

### Look-ahead and Look-behind
look-ahead and look-behind matches characters and then gives up the match returing the result. They do not consume characters in a string but only assert whether a match is possible or not.
```
look-ahead 
X(?=Y) look for X but match only when followed by Y
look-behind
X(?!Y)  lok for X but only if not followed by Y
```
## Author
 Name: Sheila Chepkemoi Kiprotich.
 https://github.com/sheilashix/Computer-Science-For-JavaScript-Regex/tree-save/main/README.md
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
