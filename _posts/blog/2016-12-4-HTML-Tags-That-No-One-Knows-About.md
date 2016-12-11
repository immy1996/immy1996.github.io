---
layout: post
title:  "HTML Tags That No One Knows About"
date:   2016-12-4 5:12:00
categories: blog
---
As I grew learning how to develop websites from my mom, that meant I learned from her about HTML. Even my mom taught
me some HTML tags that no one doesn't even know about! So I want to share some of those tags in this blog post here
and how I encountered it.

So one day I was working on a project for a class of mine and one of my tasks was to handle to login authentication. 
Then I was able to get the login error message to pop up if the login information was incorrect. So I wanted to not
make it boring and such. I asked around and found out about the HTML marquee element.

In simplistic terms, that tag is used for scrolling piece of text or image displayed either horizontally
across or vertically down your web site page depending on the settings of your site.

Here's my login authentication I used for my project:

            {% if failed %}
                <h3 style="color:#ff3333;"><center><marquee style="height:1;width:200" scrollamount="200" scrolldelay="500">Invalid username or password!</marquee></center></h3>
            {% endif %}

All I said above is that if login has failed for the user, then let "Invalid username or password!" appear on the page but let it move from right to left quick. 

<marquee>Basically like this

Another interesting HTML tag that I approached to is the <mark> tag. What this will do is that it will basically highlight your text if you put it in the <mark>
tag. An example is like this:

        `Hey guys! My name is Imran Ahmed and I LOVE the <mark>BOSTON CELTICS</mark>`
        
Which should give you your result similar to mine that I have below:
<img src="/assets/img/BostonCeltics.jpg" alt="Boston Celtics Highlight Text" height="500" weight="500">

Just wanted to share some of these HTML tags that I have learned recently! Hope you enjoyed this post!

Sources: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/marquee, https://www.tutorialspoint.com/html/html_marquee_tag.htm, http://www.w3schools.com/tags/tag_mark.asp
         