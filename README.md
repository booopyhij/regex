# regex
# Regex email matching

In this README I hope to explain regex and it's use pertaining to matching an email for verification purposes.

## Summary


I will be using the Regex for email verification as an example for describing the process of how regex works and how to best use it.
The Expression I will be using is: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/   This is the regex for email verification. I will 
explain the components of regex
Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ in this email matching expression, there are 2 anchors.
the ^ at the beginning of the expression signifies the start of the expression. This means the everything after will be included
in the search. The $/ at the end is the endpoint of the express. Everything between the /^ (this) $/ will be the search expression.
### Quantifiers
Quantifiers sets the limits of the string to be matched. for this example with email matching, there 3 sets of quantifiers.
The first and second quanitfiers are the same. it is the + at the end of the end of the bracket expression. the + is telling the expression to match the pattern 1 or more times. the second quantifier is {2,6} at the end of the third bracket expression. This is looking to match a string with a minimum of 2 characters and a maximum of 6 characters.
### Grouping Constructs
Grouping constructors look for an exact match. they are set outsiide of the parantheses. For example, (1ab):(x0) would look for a string that looks like 1ab:x0. While the parameters set inside the parantheses could be anything, the colon will always be there. In the example of email matching, there are 2 grouping constructs. The first is between the second and third bracket expression. it is the @ symbol. This @ will always be there, allowing for the seperation of 'user' and 'site of origin'. All emails use the @ symbol, so this being always defined where it is will make sure there is no other matching options. The second grouping construct is a period. This lays between the second and third bracket expression. this is to seperate the domain from the endpoint. such as gmail and com. adding this to the expression makes sure users type gmail.com instead of gmailcom . 
### Bracket Expressions
Bracket expressions are used to set a range of characters that can be used for valid matching. In the example of email
verification there are 3.
The first one is [a-z0-9_\.-] This bracket expression comes before the @. This is used to match everything before the @ symbol in an email. What this expression is searching for is: any lowercase letter a through z, any number 0-9, an underscore, and periods, and hyphens.
The second one is [\da-z\.-] comes after the @ and is looking for the website. This is looking for any digit, lowercase letters a through z, \. is looking for periods, and if there are any hyphens.
The third one is [a-z\.] comes after the . and is looking for the website endpoint. such as .com .jp .gov .co .uk .ca, etc. It is looking for a period and any lowercase letter a-z.

### Character Classes
Character classed allow for a more simplified way of writing an expression in this example the second bracket expression [\da-z\.-] uses \d . the \d acts the same way as if you were to write 0-9. There are also classes for any character and alphanumeric character and whitespace.
### The OR Operator
the or operator is | it allows for an expression to look for one or the other. There are no or operators in the email matching expression.

### Flags
Flags are placed at the end of the expression. they are used to define what strings should be tested against the expression. While there are no flags inside the expression for email verification, I would recommend adding the i flag. This allows for a case-insensitive search. many people look up email's through their phones or tablets, they usually have caps turned on auto for the first letter inserted. Using the i operator will allow an email typed as Example@example.com to be sent to example@example.com, which is the same email.
### Character Escapes
Character escapes let special charaters or characters that would be otherwise used as another operator in the expression be used as a search parameter. for example, in the email matching, \. is used in each bracket expression. the \ allows the . to be used inside the bracket expression as something to search for. 

## Author
I am a student in the coding bootcamp by EdEx. https://github.com/booopyhij
