# Regex Tutorial for URL 

If you didn't know, Regex is short for Regular expressions. Regex are useful in extracting information from text. They are used in code to match and find specific search patterns or text patterns!

## Summary

We will be exploring what each symbol means in the specific regex function for matching URL link patterns. what kind of pattern might a url link contain? Let's look at the google url link format: https://www.google.com

as we look at this link and compare it to others we can determine that a regular expression might contain https:, www, ., and maybe some kind of 3 letter decalaration of what kind of website. In fact the code we would use for the regular expression would be as follows:
``` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ ```

This may look intimidating at first but I assure you it is quite simple! Let's break it down.

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
- [Back-references/ Look-ahead and Look-behind](#back-references/look-ahead-and-look-behind)

## Regex Components

The components that make up a regular expression are as follows:

*Anchors, Quantifiers, OR Operator, Character Classes, Flags, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Match, Boundaries, Back-references, Look-ahead and Look-behind

Let's take a deeper look into each component and where they are in the URL matching regular expression.


### Anchors

Anchors in a regex are generally signaled by the symbols ```^``` or ```$```. They indicate the beginning and end of the expression. In the case of the URL matching regex, the ```^``` is found after the ```/``` but before the ```(https?:```

Where as the ending anchor is after the last `?` symbolized by the ```$```.

### Quantifiers

Quantifiers allow for specific matching strings saying it has to match with or without the last letter. in this case, we see the ? quantifier thaat allows for an exact match before before the last letter of ```https``` saying that it can have the s or it doesn't need it. 

### OR Operator

We see the or ([]) operator in our URL expression saying it can have anny letter a-z in ```[a-z\.]``` in the second half of the expression. this is saying it matches a string that has a-z followed by 2 up to 6 .

### Character Classes

In the first part of the regex, we see ```([\da-z\.-]+)``` which in short means it mush match a sigle character a-z that is a digit. We also see at the end of the expression ```([\/\w \.-]*)```, which is saying it much match a work character or an alphanumeric character including underscores.

### Flags

There are two flags, one towards the end characterized by ```/?$/``` and one in the begiinning characterized by ```\/\/```. this tells the program that there are must haves in the expression/ pattern. if we don't have them in the text in question it will not recognize it as a URL match.  

### Grouping and Capturing

In the regex epression ``` /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ ```, we see multiple groupings caracterized by (). all of the cases in the URL matching regex are creating a capturing group with the values in between the parenthesis. 

### Bracket Expressions

Bracket expressions allow for and or function with a range. For instance the bracket epression in the URL matching regex ```[a-z\.]``` allows for any character within the range a-z to be applicable. it is the same as saying a|b|c|...

### Greedy and Lazy Match

These types of quanifiers allow for an expanded range in which the match can be made through the text provided. We sadly don't see this in the URL matching regex expression...

### Boundaries

There aren't any boundries, characterized by ```\b...\b```, in our URL matching regex. They allow for a "whole words only" search. 

### Back-references/ Look-ahead and Look-behind

Back-references allow for references later and look-ahead/look-behind look for specific characters in your expression and look for either a proceeding condition or ending condition. While both are usefull neither of these appear in our expression.

## Author

Andrew Mac is a learning web developer studing through the coding bootcamp through Michigan State University. His github can be found using [this](https://github.com/Lonxyboi22) link where you might find more intuitive projects he has made. 

### Thank you for reading!
