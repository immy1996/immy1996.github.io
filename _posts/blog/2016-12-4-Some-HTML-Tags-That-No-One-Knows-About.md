---
layout: post
title:  "Some HTML Tags That No One Knows About"
date:   2016-12-4 5:12:00
categories: blog
---
As I grew learning how to develop websites from my mom, I learned from her all about HTML. My mother is a website designer.
My mom even taught me some HTML tags that no one even knows about! So I want to share some of those tags in this blog post
here and how I encountered it.

So one day I was working on a project for a class of mine and one of my tasks was to handle to login authentication. Then 
I was able to get the login error message to pop up if the login information was incorrect. So I wanted to not make it boring
and such. I remembered about the following HTML marquee element that I learned with my mother.

In simplistic terms, that tag is used for scrolling piece of text or image displayed either horizontally
across or vertically down your web site page depending on the settings of your site.

Here's my HTML login authentication code I used for my project if the user has a login error and the login error message will appear:

        <h3 style="color:#ff3333;"><center><marquee style="height:1;width:200" scrollamount="200" scrolldelay="500">Invalid username or password!</marquee></center></h3>
        
This will show the message "Invalid username or password!" and will move it from right to left on the screen.

<marquee>Basically like this</marquee>

Another interesting HTML tag that I approached to is the mark tag. What this will do is that it will basically <mark>highlight your text if you put it in the mark
tag.</mark> Here's another example:

Here's the code:

        `Hey guys! My name is Imran Ahmed and I LOVE the <mark>BOSTON CELTICS</mark>`
        
Which should give you your result similar to mine that I have below:
<img src="/assets/img/BostonCeltics.jpg" alt="Boston Celtics Highlight Text" height="500" weight="500">

Just wanted to share some of these HTML tags that I have learned recently! Hope you enjoyed this post!

Sources: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/marquee, https://www.tutorialspoint.com/html/html_marquee_tag.htm, http://www.w3schools.com/tags/tag_mark.asp
         