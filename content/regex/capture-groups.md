---
title: "Capture Groups"
date: 2020-05-07T04:28:29Z
draft: false

weight: 3
---

Capture groups are similar to character sets, but they allow matching specific character sequences and can capture part of the input.

### Matching

Capture groups allow matching entire character sequences (strings). Rather than `[abc]` matching either "a" or "b" or "c", the capture group `(abc)` matches "abc".

You can match different strings using `|` to separate different options. You can use character sets within capture groups to add additional flexibility. Since character ranges don't exist in capture groups, you do not have to escape "-", but it doesn't hurt and can make reading the regex clearer. Capture groups follow all the same multiplicity rules.

##### Examples

| Capture Group     | Matches                                                            |
| ----------------- | ------------------------------------------------------------------ |
| `(color|colour)`  | color,colour                                                       |
| `Cat(apult|-nap)` | Catapult,Cat-nap                                                   |
| `(cool[\s]?)+`    | cool,cool ,coolcool,[cool cool cool](https://youtu.be/zDcbpFimUc8) |
| `(wee\|doo)+`     | weedooweedoo,wee,doo,doodoodoo                                     |

### Capturing

Capture groups can also be used to capture (wow) a sequence of characters. This can be used to extract parts of a string or test if a substring is within a string.

Most languages allow you to evaluate a regex and then use the capture groups as variables in your code. Since this is done in different ways for each language, this will not be covered here.  
Capture groups can also be used to check for an exact match in different places in the regex. A capture group is used by placing `\1` in the regex, where `1` is the index (starting at 1) of the capture group

##### Examples

| Capture Group                    | Match(es)                               |
| -------------------------------- | --------------------------------------- |
| `(hello) \1`                     | hello hello                             |
| `(ye(haw\|et)) \1`               | yeet yeet,yehaw yehaw                   |
| `(t)(a)(c)(o)\3\2\1`             | tacocat                                 |
| `(http[s]?)://(.*)[:](\d+)/(.*)` | <http://example.com:80/an/example/path> |

You can also mark groups as non-capturing by adding `?:` to the start of the group (e.g. `(?:test)). This prevents regex parsers from waisting time pulling out strings if you do not need to use the value later.
