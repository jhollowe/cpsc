---
title: "Positions"
date: 2020-05-07T22:39:38-04:00
draft: false

weight: 4
---

Regexes can also be positionally limited. This allows you to match an entire string. It also allows matching to the beginning or the end of the sting.


| Character | Position |
|-----------|----------|
| `^`       | Start    |
| `$`       | End      |

##### Examples

| Regex    | Input  | Match(es) | Non Match(es) |
|----------|--------|-----------|---------------|
| `^test$` | test   | test      |               |
| `^test$` | a test |           | a test        |
| `^test`  | a test |           | a test        |
| `^test`  | test 2 | test      |  2            |
| `test$`  | a test | test      | a             |
| `test$`  | test 2 |           | test 2        |
