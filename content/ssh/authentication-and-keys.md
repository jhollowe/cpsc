---
title: "Authentication and Keys"
date: 2020-08-11T19:42:19-04:00
draft: true

weight: 2
---

A major part of *Secure* shell is authentication and permission management. We don't want just anyone to be able to get a shell on our machine, and we don't want any user to be able to access any other user's files or programs.

## Creating SSH Keys

SSH keys are a tool to use a public/private keypair instead (or in addition to) a password to allow for easier and automated SSH access.

To create an SSH key, use the following command to generate a modern, secure key:

```shell
ssk-keygen -t ed25519 -f ~/.ssh/name_of_your_key -C "This is an optional comment"
```

{{<alert style="info">}}ed25519 is not compatible with *very* old SSH servers. For advantages and catches of using ed25519, check out [this article for more information](https://medium.com/risan/upgrade-your-ssh-key-to-ed25519-c6e8d60d3c54#c4ec){{</alert>}}



# TODO
* `ssh-copy-id` to server
