---
layout: post
title:  "Intro to Flask"
date:   2016-11-10 02:10:00
categories: blog
---
I've been using Flask in Cloud9 to create websites and it's been very fun to do so. I'll show you what Flask is, how to install Flask via command line, and how to use Flask via Python and HTML.
It honestly isn't bad and it won't take that long!

The definition of Flask is: a Python module for writing web applications. So you need to install Flask via command line:
`sudo easy_install flask markdown`

That command above will install Flask for you and the next thing you have to do is create a server.py file (I would recommend cloud9 but you can choose the editor of your choice) and in the
server.py file, you should have this be in your py file:
`import os`
`from flask import Flask`
`app = Flask(__name__)`
` `
` `
```
@app.route('/')
def helloWorld():
    return "Hello World"
```
