# Regex - Matching an Email

Introductory paragraph:  The purpose of this tutorial is to describe a regular expression or regex.  These expressions contain a certain pattern of characters.  These patterns can be used to validate inputs.  For example, a regex can be used to validate a value or even an email address.  

## Summary

For this tutorial, I will focus on one particular regex.  This expression will focus on matching an email.  The following expression will be broken down and explained.  The following expression can be used to validate that an email is following the correct format.  For example, if a user forgets the @ symbol, the expression will notice that it is not an email address.  

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Quantifiers
Quantifiers are used to match a set of characters. For instance, quantifiers such as "a-z" will match any set of lowercase letters.  A quantifier of "0-9" will allow any set of numbers.

In the first part of our email regex, /^([a-z0-9_\.-]+), it will allow a through z lowercase letters and numbers 0-9.  It will also accept the email if it has a _ symbol, a ., or a - symbol.  Our regex also contains a + that is outside of the brackets, which means it needs at least one item.

The second part of our regex, ([\da-z\.-]+), is indicating that it needs a 

### OR Operator
An Or operator takes one side of the or operator or the other side. The Or operatior is shown as a | .
Our email regex, does not contain an Or operator so I will use a different example.   
The following is from matching a hex value. 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

The hex value will start at the #.  Then the regex will take the first side, ([a-f0-9]{6}, or the second side,[a-f0-9]{3}.  The first side, ([a-f0-9]{6}, will be a six character string with lowercase letters and numbers.  The second side, [a-f0-9]{3}, will be a three character string with lowercase letters and numbers.  

### Character Classes
Character classes take a small sequence and match it up to a larger set.  For instance, the regex can match one character in the set.   

In our email regex, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we can look at the "\d".  This will take one character from lowercase letters.  After the @ symbol, it will make sure there is a lowercase letter.  

### Flags
A flag is a parameter that is optional.  Flags change the default behavior of the search. Flags are a single i, g, s, m, y, or u.  

Each letter is a different flag. The i flag ignores casing. The g flag is global so it will search all.  There are also dot all, multiline, sticky, and unicode flags.  

Flags will come after the second /.  I included an example below.  
/.+/g

### Grouping and Capturing
Grouping and capturing is used to find a string of characters and group them.  Parts can be grouped together within parenthesis.  

If we look at the email regex, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, you will notice that first group is inside a set of parenthesis.  This is the first group, ([a-z0-9_\.-]+). The next group is in the next set of parenthesis, ([\da-z\.-]+). The last group is ([a-z\.]{2,6}).

### Bracket Expressions
Bracket expressions are used for character classes.  Brackets are used to enclose a set of characters.  A range of letters or numbers can be used within brackets.  In our email regex, /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/, we have three sets of brackets.  

Our first set, [a-z0-9_\.-], uses a range of lowercase letters. Any letters between and z can be used.  Any digit between 0 and 9 can also be used.  

Our second set, [\da-z\.-], uses and checks just the first character.  It is checking for any letter between a and z.  

Our last set, [a-z\.], can use any letter between a and z, a \ and also a . in the set. 

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

I am Matt Foster.  I designed this tutorial as part of a full-stack web development bootcamp.  When I complete the bootcamp, I am looking to find a career in web development. 

If you are interested in taking a look at my Github profile or getting in contact with me, you can find that information below.

Github: https://github.com/fmatthew40
email: fmatthew40@gmail.com
