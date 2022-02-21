# Regex - Matching an Email

Introductory paragraph:  The purpose of this tutorial is to describe a regular expression or regex.  These expressions contain a certain pattern of characters.  These patterns can be used to validate inputs.  For example, a regex can be used to validate a value or even an email address.  

## Summary

For this tutorial, I will focus on one particular regex.  This expression will focus on matching an email.  The following expression will be broken down and explained.  The following expression can be used to validate that an email is following the correct format.  For example, if a user forgets the @ symbol, the expression will notice that it is not an email address.  

Matching an Email – `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

### Anchors
To start, we will take a look at the anchors in the regex.  Anchors start and end an expression. Anchors are focused on positions rather than characters in the regex.  For example, the ^ symbol starts our expression and the $ symbol ends our expression.

We can see in the following expression, that the ^ is starting our expression.  We can also see that the $ symbol is ending our expression.  
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Quantifiers
Quantifiers are used to match a set of characters. For instance, quantifiers such as "a-z" will match any set of lowercase letters.  A quantifier of "0-9" will allow any set of numbers. 

In the first part of our email regex, `/^([a-z0-9_\.-]+)`, it will allow a through z lowercase letters and numbers 0-9.  It will also accept the email if it has a _ symbol, a ., or a - symbol. 

The second part of our regex, `([\da-z\.-]+)`, is indicating that it needs to check for a single lowercase letter, a through z.  

The third part of our regex, `([a-z\.]{2,6})`, contains `{2, 6}`.  This means it will allow 2 to 6 characters.  

### OR Operator
An Or operator takes one side of the or operator or the other side. The Or operatior is shown as a | .
Our email regex, does not contain an Or operator so I will use a different example.   
The following is from matching a hex value. 
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The hex value will start at the #.  Then the regex will take the first side, `([a-f0-9]{6}`, or the second side,`[a-f0-9]{3}`.  The first side, `([a-f0-9]{6}`, will be a six character string with lowercase letters and numbers.  The second side, `[a-f0-9]{3}`, will be a three character string with lowercase letters and numbers.  

### Character Classes
Character classes take a small sequence and match it up to a larger set.  For instance, the regex can match one character in the set.   

In our email regex, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we can look at the "\d".  This will take one character from lowercase letters.  After the @ symbol, it will make sure there is a lowercase letter.  

### Flags
A flag is a parameter that is optional.  Flags change the default behavior of the search. Flags are a single i, g, s, m, y, or u.  

Each letter is a different flag. The i flag ignores casing. The g flag is global so it will search all.  There are also dot all, multiline, sticky, and unicode flags.  

Flags will come after the second /.  I included an example below.  
`/.+/g`

### Grouping and Capturing
Grouping and capturing is used to find a string of characters and group them.  Parts can be grouped together within the set of parenthesis.  

If we look at the email regex, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, you will notice that first group is inside a set of parenthesis.  This is the first group, `([a-z0-9_\.-]+)`. The next group is in the next set of parenthesis, `([\da-z\.-]+)`. The last group is `([a-z\.]{2,6})`.

### Bracket Expressions
Bracket expressions are used for character classes.  Brackets are used to enclose a set of characters.  A range of letters or numbers can be used within brackets.  In our email regex, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we have three sets of brackets.  

Our first set, `[a-z0-9_\.-]`, uses a range of lowercase letters. Any letters between and z can be used.  Any digit between 0 and 9 can also be used.  

Our second set, `[\da-z\.-]`, uses and checks just the first character.  It checks for any letter between a and z.  

Our last set, `[a-z\.]`, can use any letter between a and z, a \ and also a . in the set. 

### Greedy and Lazy Match
Greedy and lazy matches are opposites.  A greedy match tries to make a match for every position in the string.  If there isn't a match, it will move to the next part. On the other hand, a lazy match will use a question mark (?) after a quantifier.  A lazy match will repeat as little as possible.  It may look for one or two characters that match and move on.  

Here is our email regex again, `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.
We do not have any question mark symbols in our regex so it is being run as greedy.

### Boundaries
Boundaries are positions.  For example, `\b`, can be used as a word boundary.  This means that it matches things such as letters, digits, and an underscore.  There should be a `\b` to start the word boundary and another `\b` to end the word boundary.  

Another boundary, `\B`, works the same way, except that it checks for characters that are not part of the `\b`.  

### Back-references
Back references check the same exact text as used previously.  An example of this in a regex could look like this, `\1`.  This means it will use the same text as the first capturing group.  

### Look-ahead and Look-behind
A look-ahead and look-behind are used to determine if there is a match or no match.  They are determining whether a match is possible. A look-ahead and a look-behind work similarly.  The difference is that the look-behind works backwards, versus forwards.  

## Author

I am Matt Foster.  I designed this tutorial as part of a full-stack web development bootcamp.  When I complete the bootcamp, I am looking to find a career in web development. 

If you are interested in taking a look at my Github profile or getting in contact with me, you can find that information below.

Github: https://github.com/fmatthew40
email: fmatthew40@gmail.com
