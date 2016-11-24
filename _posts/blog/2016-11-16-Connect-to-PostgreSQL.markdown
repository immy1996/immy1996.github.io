---
layout: post
title:  "Connect to PostgreSQL"
date:   2016-11-16 02:40:00
categories: blog
---

To connect to PostgreSQL, you need to use Python. But the first step you need to do 
is type this into your command:
` sudo apt-get install python-psycopg2 `

This line of code will install the adapter.

After that, open up a python file and use the following code:
```
import psycopg2

import psycopg2.extras

import os

def connectToDBServer():

    print("Connecting to the database!")
    
    connectionString = 'dbname=celtics user=iahmed password=abc host=localhost'
    
    try:
    
       return psycopg2.connect(connectionString)
       
    except:
    
       print("Can't connect to database!")
       
```

Since we're trying to connect to PostgreSQL, that's were we connect by importing the psycopg2 module
and wrote the <code>def connectToDBServer()</code> function. Within that <code> def connectToDBServer </code>
function, we made the connectionString and provided the dbname = (databasename), user = (username), password 
= (password), host= (url).

Especially, we're trying to make the connection using "<code> psycopg2.connect(connectionString)</code>" by
passing the connectionString in the beginning of our function. If it connects in the try statement, then it 
will return us the connection to the database. If not, then it will go the except statement and tell the user
by printing out that "Can't connect to the database!"

When we are connected to the database, we can fetch to the information by using this code:
```
    
    con=connectToDBServer()
    
    cur =con.cursor(cursor_factory=psycopg2.extras.DictCursor)
    
    cur.execute("select * from users where username=%s and password=crypt(%s, password);",(iahmed,pass) )
    
    loginResults=cur.fetchone()
```

With the code above, we are calling our <code> connectToDBServer()</code> function we made earlier and are storing it
into the "<code>con</code>" variable. After that, we made a cursor that allows us to execute any queries like for example
the next line after we made the cursor which allowed us to execute a query statement using the cur.execute command. We basically
executed a query statement that selects the information corresponding the username and password specifically by the user. We passed 
the query that needed to be executed as an argument. The last line of code, we are fetching that particular result since it is 
"<code>cur.fetchone()</code>" and that's storing it into the loginResults.