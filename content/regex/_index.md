---
title: "Regex"
date: 2020-05-05T03:30:27Z
draft: false

weight: 5
---


`he[l]{2}o\sth(e)r\1!`

If you can read that, you can probably skip over this section.
This section is about Regular Expressions, or Regex.

### What is Regex?

Regular expressions allow you to specify a template to match against a string. This template can
allow multiple strings to match, allowing a variable entry to match a fixed rule. Regex can also be
used to extract sections from a variable string.

Regex can be super powerful, but it can cause problems if given strings that are unexpected or malicious. Attackers can trick a regex into validating incorrect strings or pulling the
wrong thing from a string. Regex can also fail to match valid data that is in a format that
you are not expecting.

### Resources

* [https://regexr.com/](https://regexr.com/) is a great tool to check and play around with regex.
* [https://regexcrossword.com/](https://regexcrossword.com/) is a fun way to gradually learn more and more complex regexes
* [https://regexone.com/](https://regexone.com/) is an interactive guide through regular expressions

I've learned a lot from learning the basics and then learning as I solve more of the regexcrosswords.
