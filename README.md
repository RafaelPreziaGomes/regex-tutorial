# Tutorial on Regex — Email Matching

Regex, which stands for regular expression, is a string of text that may be used to search for or sometimes modify input text. It may be used to a variety of computer languages, including Javascript, and search engines, like the Ctrl+F feature in Google Docs. In this explanation, we'll look at a "basic" regex that matches any kind of email.


# Summary of Contents

- Quantifiers, Anchors, and Character Classes
- Organizing and Taking Note of Bracket Expressions
- Regex Elements
- Anchors
- Quantifiers\s+


# Summary

The regex code snippet for matching an email is as follows: `/^ ([a-z0-9_\.-]+) @([\da-z\.-]+)\.([a-z\.]{2,6}) $/`

This Regular expression expression seeks out any character group of different size and characters, followed by the sign "@," another word group of varied size, followed by a period ".," and ending with a character group with a minimum of 2 but a maximum of 6 characters. I wrote this as a handy reference for students like myself by outlining what each block of code accomplishes and what each component is specified as. Character classes, anchors, quantifiers, etc.

# Examples

- **Anchors**

Using this example, `randomtext` is an exact string match from start to finish.

This  matches a string if it has one or more copies of the previous character or sequence, whereas 2,6 matches a string if it contains at least two but not more than six copies.

Any single character that is a digit or "number" from 0 to 9 is matched by Character Classes d.

It's comparable to using `0-9`

This is literal meta char for "." @ this is literal character for "@" Unlike the period before it, "@" doesn't have any special operation associated with it, so it does need the backlash "" before it. 

This changes the period to become literal character instead of being a Greedy Operaters that matches as many characters as possible.
Organizing and Taking ([a-z0-9_]+) ([da-z]+)

- 	**Quantifies**

matches any combination of one or more characters that are letters A through Z, numbers 0 through 9, an underscore `(_)`, a period `(. )`, or a hyphen `(-)`.
Additionally, it demonstrates how to use the Quanifier '+' to expand the size of the match for the group.
`([a-z\.]{2,6})`

matches any combination of at least two (but not more than) six `(a-z)` letters or a literal period `("")`
This is a possible application of the Quanifier "2,6" to broaden the scope of the group's match.
Boundary Conditions
`[a-z0-9_\.-]`
`[\da-z\.-]`


both searches for single characters with the following characteristics: a-z, 0-9, underscore `(_)`, literal period `(. )`, or hyphen `(-)`.
`[a-z.]` matches any single character that is an actual period or the letters a through z.

# Author

Done by Rafa Prezia
