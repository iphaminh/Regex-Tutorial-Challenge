# Regex Tutorial: Understanding the Power of Patterns

This tutorial will explain how a regular expression is able to create patterns that help match, locate, and manage text. 

## Summary

Regex is a potent tool for pattern matching and searching within strings. Its primary purpose is to find, match, and manipulate text data, and it accomplishes this by using special characters and metacharacters. For example, the regex pattern /^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/ incorporates special characters and syntax. By understanding these unique elements of regex, we gain the ability to delve deeper into its components. 

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

Components of a regex matching a URL include:

Anchors 
Quantifiers 
Character classes 
Grouping and capturing 
Bracket expressions 
Greedy match

### Anchors

Anchors belong to the family of regex that dont match any character, but that affirm something about or on the string to enhance the matching proccess. For example, ^from the start to the end$ is an exact match that start at the "from" to the end of the string "end"

### Quantifiers

Quantifiers in regular expressions specify how many instances of a character or group should be matched.

?	Question Mark		  Matches zero or one preceding character.        abc?  -  ab
*	Asterisk	    	  Matches zero or more preceding characters.      abc*  -  abc and more after letter c
+	Plus Sign	        Matches one or more preceding characters.       abc+  -  abc and more after letter c
{ }	Curly Braces    Creates a specific numerical quantifier range.  {abc} - abc
{5}	Curly Braces	  Matches exactly five characters.                a{5}  - aaaaa
{2,5}	Curly Braces  Matches between two and five characters.        \a{2,5} - 12, 123,1234,12345
{2,}	Curly Braces	Matches two or more characters.                 \[a-z]{2, } - ab, abc, abcdef

### OR Operator

A logical | "or" operation in regex. For example, ^(a|b)c$ matches either "ab" or "ac".

### Character Classes

Character classes allow for specific sets of characters to be matched.

\d: Matches a single digit. E.g., /\d/ matches any single digit from 0-9.

\w: Matches letters (both uppercase and lowercase), digits, and underscores. E.g., /^\wHello123/ will match "Hello123".

\s: Matches a white space. E.g., abc\s+cdd matches the string "abc cdd".

.: Matches any character except for a newline. E.g., c.t matches "cat", "cot", "cut", etc., but not "caat" or "ct".

### Flags

Flags are used to alter the search pattern. They follow the closing slash of the pattern and are denoted by single letters.

/i: Case-insensitive search. E.g., /abc/i matches "abc", "Abc", "ABC", etc.

/g: Global search. Without it, the regex will stop after the first match. E.g., /abc/g matches all instances of "abc" in a string.

/m: Multi-line search. Changes the behavior of ^ and $ to match the start or end of a line, not just the string. E.g., /^abc/m matches "abc" at the beginning of any line.

### Grouping and Capturing

Grouping is done using parentheses (). It groups parts of the regex together and captures the matched content for use with back-references.

(\d{3})-(\d{4}): Matches and captures phone numbers in the format "123-4567".

### Bracket Expressions

Bracket expressions [] match any one of the characters inside the brackets E.g [adde] will match any instances in the []

### Greedy and Lazy Match

Quantifiers are greedy by default, matching as much as possible. Lazy match, on the other hand, matches as little as possible.

a.+b (greedy): In "aXYZbXYZb", matches the entire string.

a.+?b (lazy): In "aXYZbXYZb", matches only "aXYZb".

### Boundaries

\b is a zero-width assertion that matches the position between a word character and a non-word character.

\w+ing\b match " i love eating 'checkenwings'"

### Back-references

Back-references allow you to refer to previously captured groups in your regex.

string {apple fruit orange citrus} with (apple|orange).*? - apple fruit , orange citrus

### Look-ahead and Look-behind

Look-aheads and look-behinds are zero-width assertions that let you check for a pattern without including it in the match.
q(?=u): Matches the "q" in "queen" but not the "q" in "qatar".
(?<=a)b: Matches the "b" in "cab" but not the "b" in "tube".


## Author

My Profile https://github.com/iphaminh
