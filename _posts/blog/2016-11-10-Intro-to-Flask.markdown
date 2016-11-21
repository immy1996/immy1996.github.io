---
layout: post
title:  "Intro to Flask"
date:   2016-11-10 02:10:00
categories: blog
---
I've been using Flask in Cloud9 to create websites and it's been so fun. I'll tell you what Flask is, show how to install Flask via command line, and how to use Flask via Python and HTML
and you'll be able to create simple pages. It honestly isn't that hard and it won't take that long to get a website up and running!

The definition of Flask: a Python module for writing web applications. So you need to install Flask via command line: `sudo easy_install flask markdown`

The next thing you have to do is create a server.py file (I would recommend cloud9 but you can choose an editor of your choice) and in the
server.py file, you should have this in your server.py file to create your first page:


    import os
    
    from flask import Flask
    
    app = Flask(__name__)
    
    @app.route('/')
    
    def helloWorld():
    
        return "Hello World"
     
    
    #start the server
    
    if __name__ == '__main__':
         app.run(host=os.getenv('IP', '0.0.0.0'), port=int(os.getenv('PORT', 8080)), debug=True)


If you run the server and get the link that you get from you terminal, you should get the same result as I get in this picture below:
<img src="/JekyllGithubTechnicalblog/sleek_blog-master/assets/img/IntroToFlaskBlog2.jpg" alt="Hello World Example 3">

You can in this case in your server.py file, you can use a bit of HTML code to make it more better than it being plain text like this:

```
import os

from flask import Flask

app = Flask(__name__)

@app.route('/')

def helloWorld():

    return "<h1 style=\"color:red\">Hello World</h1>"
    

#start the server

if __name__ == '__main__':
     app.run(host=os.getenv('IP', '0.0.0.0'), port=int(os.getenv('PORT', 8080)), debug=True)
```

What that will do up there will change the size of the text bigger and change the color to red. So if you did what I did above, you should get the same result as I did in this picture below:
<img src="/JekyllGithubTechnicalblog/sleek_blog-master/assets/img/HelloWorldColorChange.jpg" alt="Hello World Color Change Example">

If you wanted to make more than one page, all you have to do is with this code below:

```
import os

from flask import Flask

app = Flask(__name__)

@app.route('/')

def helloWorld():

    return "<h1 style=\"color:red\">Hello World</h1> Welcome to my website! Click here to find about <a href=\"about\">me!</a>"
    
@app.route('/about')

def aboutMe():

    return "<h1>About me!</h1> Favorite basketball team: Boston Celtics"
    
#start the server

if __name__ == '__main__':
     app.run(host=os.getenv('IP', '0.0.0.0'), port=int(os.getenv('PORT', 8080)), debug=True)
```

This will simply create and allow you to switch to your about page you have in "`@app.route('/about')`". If you did what I did above, you should get the same results as I did in these pictures:
<img src="/assets/img/HelloWorldColorChangeLink.jpg" alt="Hello World Color Change Link Example 2">

Then once you click on "me", you should get this page:
<img src="/assets/img/HelloWorldColorChangeLink2.jpg" alt="Hello World Color Change Link 2 Example 2">

If you want to put HTML code in an HTML file, but first you need to connect from within your server.py file to your HTML file by using the "<a>" tag like this below:

```
<a href="/">Home<a>

<a href="/about">About me<a>
```

This will allow you to change pages by selecting either one of those two tabs (Home/About me).