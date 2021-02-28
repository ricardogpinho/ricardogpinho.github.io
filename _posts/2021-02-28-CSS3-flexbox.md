---
layout: post
title:  CSS flexbox
date: 2021-02-28 19:48:00
description: I finally took some time and learned CSS3 flexbox, it was easier than I expected
---

I learned CSS2 many years ago, back in 2007 if I remember. I made a simple website for the theater club I was involved at school at the time. I remember I'd built a flash website in the year 2006, and the next year, with the intention of learning HTML and CSS I built a new one using those technologies. Also I began learning some PHP in those years.

Well, years passed and I never looked back at CSS again, but just watching today's very responsive websites, I'm always wondering how complex is the styling underneath. 

Today I decided to take a look at the flexbox technology of CSS3. Turned out to not be much difficult.

To make use of flexbox we just need to style some html element with the property `display: flex`. Every child of this element will be affected and displayed as *flex*. Usually people classify this first element the `class="container"`.

Then we have a bunch of properties we can add to the child elements in order to control the layouts. I will not list them all here because there are many websites you can check this, but they aren't many and they aren't difficult to understand.

Another thing I also learned was media queries. `@media ... (...)`.
That isn't difficult at all as well, you can affect your layouts for printing, different screen sizes, and speech, dynamically only with this queries. For example:

```CSS
@media screen (max-width: 400px;){
	body {
		background-color: blue;
	}
}
```

In the example above, every time our screen width is bellow *400px* the background color will be blue, if we resize the window above that value, the background color will change to the default color we had previously set in our CSS file.

We can make layouts change dynamically with this.

That was it for today. 