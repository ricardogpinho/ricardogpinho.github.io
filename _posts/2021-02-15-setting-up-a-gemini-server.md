---
layout: post
title:  setting up a gemini server
date: 2020-09-28 21:01:00
description: using a raspberry pi as a gemini server
---

So, as soon as I heard about Gemini and saw in what it consists, I knew I had to jump on the train and set-up my own server and own *webpage*.

For those who aren't familiar with Gemini, Gemini is a new Internet protocol for transferring rich text. Similar to HTTP but, in many ways, different... Gemini aims to be what HTTP and HTML were in the past, in the very early days of the Web. In the early days, the *World Wide Web* was very simple and humble. Different from what we have today, there weren't dynamic pages, cascading style sheets and there was very little javascript. Internet was in fact very simple and humble, a place for the curious minds and a place you'd encounter a genuine passion driven community.
Today the web is filled with disposable content, with all sorts of people and communities gathering in a chaos that seems to have no end. That's where Gemini comes in:

Where the HTML protocol has web pages, the Gemini protocol has capsules.
An HTML web page, usually, ends in `.html`. A Gemini capsule page ends in `.gmi`.
The syntax is very simple. In 10 minutes you can learn about 90% of the syntax. It's very similar to Markdown.

So, today I embargoed in this quest of setting up my own Gemini server and serving my very first capsule.

The goal was to put the server running on a Raspberry Pi I had laying around with no use for a long time.
The good thing, I already had the Raspberry with the operating system installed on the SD card. So, that was a good start.

Then, I had to choose a server for it to run. That's when I started to face the some difficulties.

I knew [Agate](https://github.com/mbrubeck/agate) was a good server for reference on the Internet, and I did previously tested it on my main computer. It was simple and easy. The problem was, *Agate* is written in *Rust* and the Raspberry doesn't come with it installed, nor even has it in it's repositories. I thought cloning *Rust* from it's git page and compiling it and installing it, but... I thought that wouldn't be easy, once the Raspberry Pi uses an ARM V6 architecture. So I immediately discarded that option. Probably it would be possible, but with so many Gemini servers to choose I certainly could find another one not written in *Rust*.

After some tries and research I landed on the [jetforce](https://github.com/michael-lazar/jetforce), which is written in python. That's good, RPI comes with Python...

I followed the instructions provided on the *jetforce* repository and in 20 minutes I had my server running locally.
The problem arrived when I tried to make the server run as a service in Linux. I wanted for it to start even if the Raspberry Pi restarted.
But following the instructions of the repository, something wasn't working.
After about 2 hours into this, I decided to open an issue in the repository, explaining my trouble. Luckily, and gratefully, the owner replied me very quickly, with very clear instructions. Turned out it was only an user thing of Linux. I was launching the service as root instead from an user apparently.

If you want to learn more about Gemini, [here](https://gemini.circumlunar.space/) is most of what you need to know. Servers, clients, how it works and what it purposes. I am still learning too. As well learning how to write blogs... and good english :\

That's it for now. If you did read everything up to this point, I hope I haven't broken your English and if you want to check my personal Gemini capsule you can check it with an appropriate [client](https://github.com/kr1sp1n/awesome-gemini#clients). My capsule is [gemini://ricardogpt.ddnsfree.com](gemini://ricardogpt.ddnsfree.com). And if you want to set up your own, you can find a numerous of servers also [here](https://github.com/kr1sp1n/awesome-gemini#servers).