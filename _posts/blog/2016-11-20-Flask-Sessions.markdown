---
layout: post
title:  "Flask Sessions"
date:   2016-11-20 12:36:00
categories: blog
---
What session variables are is that it is stored onto the server. So they are useful in a way that if you want to
keep a user logged in on your site or to personalize what each user sess while they are logged in. The way 
"cookies" work for websites is that they are just little pieces of information that websites use to track 
a user to where they are and see their current "session" on a website.

Cookies have no expiration date, they die when the session ends. A session can end when you close the browser. Cookies
can persist even when you close your browser. Sessions are good for tracking users. Session is defined as the data in 
a session is stored in a Python dictionary. To change it up a bit, you need to create a new key and store some value
in that session like this:

    session['firstName'] = firstName
    session['lastName'] = lastName
    
So in order to use session variables, you need to start a session like this in your server.py file:

    from flask import Flask, session
    import os
    app.secret_key = os.urandom(24).encode('hex')

The way to set up session variables:

    session['username'] = 'iahmed'
    session['city'] = 'Geneva'
    session['favNum'] = 16

We can using a session variable value like this:

    print(session['username'])
    query = cur.mogrify('SELECT * FROM users WHERE name= %s', session['username'])

The best way to delete a session variable is this:

    session.pop('name', None)
