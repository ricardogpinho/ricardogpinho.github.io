---
layout: post
title:  ssh certificates
date: 2021-02-16 20:10:00
description: today I discovered SSH key-based authentication.

---


Following my project on my Raspberry Pi from yesterday, I found myself permanently *'SSHing'* in my Raspberry Pi. Every time I logged in into it I had to insert my password, obviously.
But today I stumbled upon key-based authentication. And I'm never going back to passwords!
Key-based authentication is very similar, I think, to the S in the HTTPS protocol, i.e. the encryption bit of the thing.

In key-based authentication there is a private key and a public key. They both are related.
The computer holding the server grants access to a public key. The private key stays on the client for encryption purposes.

In order to generate such pair of public-private key there is a neat command in Linux called `ssh-keygen`. Usually this command is used with the flags `-t -b`

* `-t` stands for the type, and usually `rsa` is the preferred choice.
* `-b` stand for the key size in bits. `2048` is the default, but often `4096` is used.

So, in order to generate a pair of keys the following command is usually used: `ssh-keygen -t rsa -b 4096`.
This generates the keys and puts them in the `/home/{username}/.ssh/` directory in our computer.
The next step is to give our public key to the server, so it allows us in.
There are many ways to do this, but the aim is to put our public key in the default ssh directory of the server computer in the file `/home/{username}/.ssh/authorized_keys`. We can copy our key into this file manually and give it the right permissions, but the easiest way to do this is to run a command on the terminal of the computer in which we generated the keys:

`ssh-copy-id -i /home/{username}/.ssh/{name_of_our_key.pub} user@host`

* `-i`flag is to identify the key to be sent to the host
* `user@host` is our user and server computer

Simple as that, our public key was added in the `~/.ssh/authorized_keys` in our server.

The next time we attempt to login no password will be required.

I went a little further and made an alias to my connection. By simple typing `sshpi` I'm now logged in!

