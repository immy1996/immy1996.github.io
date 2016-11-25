---
layout: post
title:  "Simple PostgreSQL Functionality"
date:   2016-11-13 8:22:00
categories: blog
---
Create, Insert, Select, Delete in PostgreSQL

To create a database in PostgreSQL, you would type this command out:
    `CREATE DATABASE users;`

I would recommend to put `DROP DATABASE IF EXISTS user;` in case if you have the same database
called user because you don't want to have two user databases.

In order to create a table in PostgreSQL, this is the basic syntax and format:

    CREATE TABLE table_name(
        column1 datatype,
        column2 datatype,
        column3 datatype,
        .....
        columnN datatype,
        PRIMARY KEY( one or more columns )
    );
From the format above, we're naming the table and giving how many columns that we want. We also are defining the column
type and the max length of that particular field data.

We'll create a simple table here:

    CREATE TABLE registered (
        account_id serial PRIMARY KEY,
	    name varchar(20),
        email varchar(100),
        age integer,
        username varchar(20),
        password varchar(20),
    );

To see our table, we will use the "\d" command in PostgreSQL which should describe our table like this:
    \d registered;
    
The format of our table:
                           List of relations
     Schema |          Name              |   Type   |  Owner   
    --------+----------------------------+----------+----------
     public | registered                 | table    | postgres
     public | registered_id_seq          | sequence | postgres
    (2 rows)

Now from above, we have our registered table, but there is also something right below our table. That is called
`registered_id_seq` which is of the type sequence. This keeps track of the next number in the sequence.

Since we have our table created, we can start inserting some data into it. For example, let's add another account
into it. We do this by calling the table that we want to add too, naming the columns and then providing
data for each of those columns. When you insert a statement, column names shouldn't be quote but the column values
that you're entering do need to be quoted but some doesn't need to like for example, our age column. We should be inserting it like this:

`INSERT INTO student_info (name, email, age, username, password) values ('Imran Ahmed', 'example@example.com', 20, 'celticsuser', 'celticspass');`

Before you always insert anything, never enter a value for any of the id column. The reason is that because it
is auto-generated whenever a new row in the table is created. 

We can select like this to get the information back:
`SELECT * from registered WHERE account_id = '1';`

Then it should display as this:

     account_id	|    name     |  age  |   username    |   password
     1	          Imran Ahmed    20      celticsuser     celticspass  
 
Now see how in the beginning our `account_id` is filled along the rest of our other data that has been organized correctly. Now let's say
we want to remove a row from our table. Let's delete the row that we just inserted into our table. We can delete it like this:

    DELETE FROM registered WHERE age = 20;

