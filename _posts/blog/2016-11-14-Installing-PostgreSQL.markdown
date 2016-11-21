---
layout: post
title:  "Installing PostgreSQL"
date:   2016-11-14 06:30:00
categories: blog
---
Now since we all know what PostgreSQL is, I can now teach you from what I learned from 
my Computer Science 350 class (Applications of Databases) on how to install PostgreSQL
and after installing it you will need to log into the default account in order to use 
PostgreSQL.

install it via command line
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib 

after installation you need to start the postgresql on your machine via command line
sudo service postgresql start

in order to use postgresql, you need to make an account. We'll login to the default account to use postgresql:
psql -U postgres -h localhost

after getting in, you can set a password via command line:
\password postgres