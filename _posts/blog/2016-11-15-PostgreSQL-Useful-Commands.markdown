---
layout: post
title:  "PostgreSQL Useful Commands"
date:   2016-11-15 01:10:00
categories: blog
---
Since now I taught what is PostgreSQL and how to install it, I'll give some helpful commands that can 
help you out when you're going to use postgres:
<ul>
<li>
Let's say if we want to login as a different user (for example, guest1) to a database (food) that you have and want to go to,
well you would write it like this:
<code>`psql -U guest1 -d food -h localhost`</code>
</li>

<li>
If you want to exit out of the postgres client account, you would type out this command:
`\q`
</li>

<li>
We can list all the databases by typing this out:
`\l` or `\list`
</li>

<li>
To change into a particular databse, you can type this out:
`\c food`
</li>

<li>
In order to show a list of tables that is in your current database that you are in, you would type this out:
`\d` or `\dt`
</li>

<li>
To describe the format of a particular table, this is the command to use:
`\d dogs`
</li>

<li>
To describe <i>in more detail</i> the format of a particular table, you would be typing this out:
`\d+ dogs`
</li>

<li>
To import sql commands from an sql file, you can type out:
`\i celtics.sql`
</li>

<li>
To delete a particular database, just type this out:
`DROP DATABASE celtics`
</li>

<li>
To show all the data in a table of your choice, just type this out:
`SELECT * FROM europe`
</li>

</ul>