---
layout: post
title:  "PostgreSQL Useful Commands"
date:   2016-11-15 01:10:00
categories: blog
---
Since now you know what is PostgreSQL and how to install it, you'll learn some helpful commands that can 
help you out when you're going to use PostgreSQL:
<ul>
<li>
Let's say if we want to login as a different user (for example, guest1) to a database (food) that you have and want to go to,
well you would write it like this:
<code>psql -U guest1 -d food -h localhost</code>
</li>

<li>
If you want to exit out of the postgres client account, you would type out this command:
<code>\q</code>
</li>

<li>
We can list all the databases by typing this out:
<code>\l</code> or <code>\list</code>
</li>

<li>
To change into a particular databse, you can type this out:
<code>\c nba</code>
</li>

<li>
In order to show a list of tables that is in your current database that you are in, you would type this out:
<code>\d</code> or <code>\dt</code>
</li>

<li>
To describe the format of a particular table, this is the command to use:
<code>\d celtics<code>
</li>

<li>
To describe <i>in more detail</i> the format of a particular table, you would be typing this out:
<code>\d+ celtics</code>
</li>

<li>
To import sql commands from an sql file, you can type out:
<code>\i nba.sql</code>
</li>

<li>
To delete a particular database, just type this out:
<code>DROP DATABASE nba</code>
</li>

<li>
To show all the data in a table of your choice, just type this out:
<code>SELECT * FROM celtics</code>
</li>

</ul>