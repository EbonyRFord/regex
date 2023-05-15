# Regggiee

The following is a regex tutorial that will explain a regex expression that is used for matching emails. I will outline in detail what each part of this expression means and explain any overlapping terms. 

## Summary

sample regex: r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b'


The regex expression r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b' 

is going to look to match email addresses by looking for uppercase & lowercase characters and numeric characters in the email address. It will also look for dots, underscores, percent signs, plus and minus signs, and a singular @ symbol. 

The domain of the email address will need to have at least one dot and be at least 2+ characters long. The \b metacharacter at the front and end of the expression ensures that the pattern matches the full email address and not just parts of it.

So, the regular expression is essentially looking for a pattern that matches the format of a typical email address: local_part@domain_name.top_level_domain.


## Table of Contents

- [Components](#components)
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

### Components

The regex components of the expression are:

\b 
[A-Za-z0-9._%+-]+ 
@ 
[A-Za-z0-9.-]+ 
\.
[A-Z|a-z]{2,}
\b 

### Anchors

Anchors are metacharacters that match a specific position within a string;they help to make regular expressions more precise and less prone to false matches. 

There are two types of anchors:

The caret ^ anchor: This matches the beginning of a line or string. If used at the beginning of a regular expression, it ensures that the pattern occurs at the beginning of a line or string.

The dollar sign $ anchor: This matches the end of a line or string. If used at the end of a regular expression, it ensures that the pattern occurs at the end of a line or string.

The \b metacharacter matches word boundaries, which are positions between a word character (as defined by the \w metacharacter) and a non-word character (as defined by \W). In this case, the \b metacharacters at the beginning and end of the expression ensure that the regular expression matches complete words, which in this case are complete email addresses.

So, the regular expression will match only if the pattern occurs at the beginning or end of a word, which means it will match only complete email addresses and not partial email addresses within larger words or phrases.



### Quantifiers

A quantifier is a metacharacter that specifies how many times a character or a group of characters can occur in a string. Quantifiers are used to match patterns of different lengths, from a single character to a potentially infinite number of characters.

In  r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', there are three quantifiers:

+ is a quantifier that matches one or more occurrences of the preceding character or character set. In this case, it is applied to the character set [A-Za-z0-9._%+-], which matches one or more occurrences of alphanumeric characters, dots, underscores, percent signs, plus and minus signs.
+ is also applied to the character set [A-Za-z0-9.-], which matches one or more occurrences of alphanumeric characters, dots, and hyphens.
{2,} is a quantifier that matches two or more occurrences of the preceding character or character set. In this case, it is applied to the character class [A-Z|a-z], which matches uppercase or lowercase letters. It ensures that the top-level domain of the email address is at least two characters long.

### OR Operator

In the regular expression r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b',

The "or" operator is represented by the vertical bar | inside a character set or character class, which is enclosed in square brackets []. In this regular expression, the character class [A-Z|a-z] matches any uppercase or lowercase letter.

So, the regular expression matches email addresses that have a top-level domain of at least two letters, and the top-level domain can be either uppercase or lowercase.

### Character Classes

In r'\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b', there are two character classes:


A character class is a set of characters enclosed in square brackets []

[A-Za-z0-9._%+-]: This character class matches any uppercase or lowercase letter, digit, dot, underscore, percent sign, plus sign, or minus sign. It occurs immediately after the word boundary \b and is followed by the + quantifier, which means that it matches one or more occurrences of the characters in the character class.
[A-Z|a-z]: This character class matches any uppercase or lowercase letter. It occurs after the dot . and is followed by the {2,} quantifier, which means that it matches two or more occurrences of the characters in the character class.

### Flags
N/A

### Grouping and Capturing
N/A

### Bracket Expressions

Bracket expressions and character classes are the same thing in the context of regular expressions, therefore:

The first bracket expression is [A-Za-z0-9._%+-], which matches any uppercase or lowercase letter, digit, dot, underscore, percent sign, plus sign, or minus sign.

The second bracket expression is [A-Z|a-z], which matches any uppercase or lowercase letter. This bracket expression occurs in the last part of the regular expression, which matches the top-level domain of the email address.


### Greedy and Lazy Match

Greedy matching is the default behavior of regular expressions, in which the expression matches the longest possible substring that satisfies the pattern. In this expression, the + quantifier in [A-Za-z0-9._%+-]+ is greedy, so it will match one or more occurrences of any of the characters within the square brackets, as many times as possible.

### Boundaries

Boundary matching is also used in this expression, using the \b anchor to match word boundaries. The \b matches at the position between a word character (as defined by \w) and a non-word character, or at the beginning or end of the string if it is preceded or followed by a word character. This ensures that the email address is matched as a complete word, rather than as part of a larger word.

### Back-references
N/A 

### Look-ahead and Look-behind
N/A 

## Author
Ebony Ford -
Lifelong learner and fitness enthusiast. 

Github profile: https://github.com/EbonyRFord



