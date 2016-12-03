---
layout: post
title:  "Installing PostgreSQL"
date:   2016-11-14 06:30:00
categories: blog
---
Now since we all know what PostgreSQL is, I can now teach you from what I learned from 
my Computer Science 350 class (Applications of Databases) on how to install PostgreSQL
and after installing it you will need to log into the default account in order to use 
PostgreSQL. It's very easy and quick to install!

On your command line, you should type out these commands:

    sudo apt-get update

    sudo apt-get install postgresql-contrib-9.3


After installation, you need to start the postgresql on your machine via command line:
`sudo service postgresql start`
This command above will start up the server. 

In order to use postgresql, you'll need to login to the default account (client) to use postgresql:
`psql -U postgres -h localhost`

After getting in, you can set a password via command line:
`\password postgres`

That's how you basically install postgres via command line! 