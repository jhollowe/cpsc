---
title: "Regex Basics"
date: 2020-05-06T01:44:39Z
draft: false

weight: 1
---

Regular expressions are a specially formatted string that has special rules used to match and extract data from strings.

{{< alert style="info" >}}**Note:** different languages can have slight differences in their implementation of regex. Make sure you test final regexes against your actual language.{{< /alert >}}

### Characters and Digits

Regexes use some characters as special characters which add functionality. If you need to use the character without its special meaning, you can escape it with a backslash "\". 

| Character Sequence | Special Function                                           | Usage                 | Match(es)              |
|--------------------|------------------------------------------------------------|-----------------------|------------------------|
| .                  | Matches any character except a line break (\n or \r)       | `gr.y`                | gray, gr_y, grHy, gr4y |
| \w                 | Matches any "word" character: alphanumerics and underscore | `\w\w\w`              | 4a_                    |
| \d                 | Matches any digit: 0 through 9                             | `I'm \d\d years old`  | I'm 04 years old       |
| \s                 | Matches any whitespace character: space, tab, and newline  | `Hello\sthere\sworld` | Hello there<br>world   |
| \W                 | Inverse of \w                                              | `\W\W\W`              | -.*                    |
| \D                 | Inverse of \d                                              | `\D\D\D`              | A%z                    |
| \S                 | Inverse of \s                                              | `ab\Sd`               | ab$d                   |
| \\                 | the backslash character                                    | `\\`                  | \                      |

By default, regexes are also case-sensitive. Therefore, if you want to match "Hello" and "hello", you can use [Character Sets](./#character-sets) to to allow both an uppercase
and lowercase letter or set the regular expression to be case insensitive. See your language's method off doing this (case-insensitivity is often the "i" flag).

### Character Sets

With regex, you can specify character sets which will match any of the included characters. This allows you to handle some basic variability.

Character sets are denoted by `[]` surrounding characters. They allow any single character within them to be matched. The best way to explain character sets is through an example.  
`gr[ae]y` matches both "gray" and "grey".

 Character sets support all the special character sequences listed above. Character sets also support character ranges. If you want to match only whole numbers, you could use `[1-9]` and if you wanted only letters, you could use `[a-zA-Z]`.

| Character range | Matches           |
|-----------------|-------------------|
| `a-z`           | a,b,c,d,...,x,y,z |
| `A-Z`           | A,B,C,D,...,X,Y,Z |
| `0-9`           | 0,1,2,...,7,8,9   |

#### Inversion/Negation

Character sets can be inverted to match everything *except* what is in the character set. This is done by having "^" as the first character in inside the brackets. To match a "^", it can be escaped ("\^").

| Character set | Matches     |
|---------------|-------------|
| `[abc]`       | a,b,c       |
| `[^abc]`      | A,$,.,4,... |
| `[\^a]`       | a,^         |
