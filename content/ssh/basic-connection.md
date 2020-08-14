---
title: "Basic Connection"
date: 2020-08-11T19:37:28-04:00
draft: true

weight: 1
---

### Basic Command

The most basic format of a ssh connection is `ssh <ip or hostname>` You will often use the ip address to connect to machines on your own network or in a cloud environment and will use a hostname to access public servers. For example, To connect to my desktop from my laptop (while they are both at home) I would use `ssh 192.168.0.100` but to connect to a cloud server I might use `ssh server.example.com`

Using this basic command will connect to the server on the default port (22) with your current user's username and start an interactive shell with the default shell for that user on the server.

If you just want to run a command on the server, you can simply append the command in quotes after the ssh command. You have to be careful about any quotes in your command and other [escaping problems]({{< ref "/shell/escaping.md" >}})

### Specifying Username and Port

While the basic command is useful if you use a consistent username across computers, often you will need to access a different user on the remote computer. Adding `<username>@` before the ip or hostname allows you to connect to the specified user on the remote (e.g. `ssh someone@server.example.com`). You can also @TODO@
