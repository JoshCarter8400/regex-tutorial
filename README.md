# Match an email regex tutorial

This is going to be a tutorial on a regular expression that matches emails. We are going to go through each aspect of the expression and describe the individual parts and what their purpose and function are.
by the end of this tutorial you will have a better understanding of how regex works and what it can be used for.

## Summary

A regular expression is a sequence of characters that defines a search pattern. Some of the uses of regex are to find patterns in strings, locate and
replace characters in a string as well as validating input which this particular one is used for. The following is the expression we wil be breaking down
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors belong to the family that don't match any characters but assert something about a string as well as the current position in the string matches a determined location.
In this example the `^` indicates the beginning of the string and the `$` indicates the ending of the string. You can read more about Anchors
at the following link [All about Anchors in Regex](https://www.regular-expressions.info/anchors.html)

### Quantifiers

The function of quantifiers is to specify how many instances of a character, group, or class must be present for a match to be found. In our example the `+` operator
is connecting the username + email provider + .com or specified address. Our other quantifier is the `{2,6}` which will allow a match in the range of
2-6 characters fromm the set of `[a-z\.]` for the dot provider we don't think that it would ever be more than 6 characters. You can read more about
Quantifiers at the following link [All about Quantifiers in Regex](https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions)

### Character Classes

Character Classes or Sets are telling the regex engine to match only of out of several characters we do this by pacing the desired character in square brackets.
In our expression the character class is `\d` which is matching a single character that is a number from the range of 0-9. It is only matching a single digit so it will
match "7" but not "77". You can read more about Character Classes at the following link
[All about Character Classes in Regex](https://www.regular-expressions.info/charclass.html)

### Grouping and Capturing

When we place parentheses around a part of a regex we are grouping that part of the expression together. This allows us to apply our
quantifiers to that group as well as restricting the alternation of that part. In our expression that we are covering we have 3 Capturing groups.
Group #1 is `([a-z0-9_\.-]+)` which is matching the user's email name. Group #2 is `([\da-z\.-]+)` which is matching the email service
provider. Group #3 is `([a-z\.]{2,6})` which is capturing the .com. You can read more about Grouping and Capturing at the following link
[All about Grouping and Capturing in Regex](https://www.regular-expressions.info/brackets.html)

### Bracket Expressions

We use bracket expressions to be able to match specific characters and set specific ranges to search within. In our expression the set
of `[a-z0-9_\.-]` is matching any letter a-z and is case sensitive and we are also matching any numbers in the range 0-9 along with the underscore,
minus sign and period symbols. We are also using `[\da-z\.-]` here we are matching a single number in the range of 0-9 and any character
a-z and is case sensitive as well along with the period and minus symbols. Lastly we are using `[a-z\.]` to match any character a-a again
case sensitive along with the period symbol. You can read more about Bracket Expressions at the following link
[All about Bracket Expression in Regex](https://www.regular-expressions.info/posixbrackets.html)

### Greedy and Lazy Matching

The standard quantifier in regex are greedy which means that they match as much as they can and only giving back as much as what is needed to match the remainder of
the expression. We can also use a lazy quantifier which just simply means that the expression tries to match as just the minimum first.
In our expression we are using greedy matches when we use the `+` quantifier since it is matching as much as possible and returning as needed.
Our second greedy quantifier is the `{}` that we use in the last capture grouping. You can read more about greedy and lazy matching at the
following link [Greedy and Lazy Quantifiers](https://javascript.info/regexp-greedy-and-lazy)

### Boundaries

There are no boundaries used in our email matching regex but I wanted to include some material on them as well. A Boundary can occur in one of 3 place

1. Before the first character in the string, if the first character is a word character.
2. After the last character in the string, if the last character is a word character.
3. Between two characters in the string, where one is a word character and the other is not a word character.
   You can read more about boundaries at the following link
   [All about Boundaries](https://www.regular-expressions.info/wordboundaries.html)

### Back-references

There are no back-references used in our email matching regex but I wanted to include some material on them as well.
Back-references match the same text as previously matched by a capturing group. You can read more about boundaries at the following link
[All about Back-references](https://www.regular-expressions.info/backref.html)

### Look-ahead and Look-behind

There are no Look-ahead and Look-behinds used in our email matching regex but I wanted to include some material on them as well.
Sometimes we need to find only those matches for a pattern that are followed or preceded by another pattern.
There’s a special syntax for that, called “lookahead” and “lookbehind”, together referred to as “lookaround”.
You can read more about Look-ahead and Look-behinds at the following link
[All about Look-ahead and Look-behinds](https://www.regular-expressions.info/lookaround.html)

## Author

My name is Josh Carter and I hope that this tutorial sheds some light on how to use a regular expression to match an email and how each part of it functions.
If you would like to view any of my other projects please feel free to follow the link to [My Github Profile](https://github.com/JoshCarter8400)
