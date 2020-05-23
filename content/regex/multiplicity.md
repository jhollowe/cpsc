---
title: "Multiplicity"
date: 2020-05-06T23:07:55Z
draft: false

weight: 2
---

Character sets are great, but many times you want to be able to specify the characters to match and _how many times_ those characters will appear.
This is where multiplicity

### Basic Multiplicity

Adding a multiplier character to the end of a character set (or a later-learned capture group) allows matching the same character(s) multiple (consecutive) times.

| Character | Multiplier |
| --------- | ---------- |
| `\*`      | 0 or more  |
| `+`       | 1 or more  |
| `?`       | 0 or 1     |

##### Examples

| Regex       | Match(es)      |
| ----------- | -------------- |
| `colo[u]?r` | color,colour   |
| `a[bcd]?e`  | ae,abe,ade,ace |
| `a[h]+`     | ah,ahhhhhhhh   |
| `[s]*h`     | h,sh,ssssh     |

### Multiplicity Ranges

You can also specify a specific multiplicity or range of multiplicity for a character set.

| Multiplicity | Number of Occurences |
| ------------ | -------------------- |
| `{3}`        | exactly 3            |
| `{2,5}`      | 2, 3, 4, or 5        |
| `{4,}`       | 4 or more            |

So `he[l]{2,5}o` will match "hello" through "helllllo".
