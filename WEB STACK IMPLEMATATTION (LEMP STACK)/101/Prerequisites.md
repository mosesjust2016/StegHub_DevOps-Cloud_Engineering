## Download and Install Git Bash 

# Download the Git Bash setup from the official website: https://git-scm.com/

* Download the installer.
* Run the .exe file you just downloaded and follow the instructions in the installer. ​
* Run Git Bash by right-clicking on any folder and selecting the Git Bash Here option from the context menu(right-click menu).

<img src="../images/git-bash.PNG" alt="Git Bash">


* 1. Open EC2 in Git Bash

```bash
    ssh -i "<Your private-key.pem>" ubuntu@<EC2-Public-IP-Address>
```

<img src="../images/open-ec2-git.PNG" alt="Open EC2">


# SELF STUDY

# SQL Syntax and most commonly used commands

# SQL Statements

Most of the actions you need to perform on a database are done with SQL statements.

SQL statements consists of keywords that are easy to understand.

The following SQL statement returns all records from a table named "Customers":

Example
```bash
    Select all records from the Customers table:
    SELECT * FROM Customers;
 ```

# Keep in Mind That...

    SQL keywords are NOT case sensitive: select is the same as SELECT
In this tutorial we will write all SQL keywords in upper-case.

# Semicolon after SQL Statements?

Some database systems require a semicolon at the end of each SQL statement.

Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

# Some of The Most Important SQL Commands

    SELECT - extracts data from a database
    UPDATE - updates data in a database
    DELETE - deletes data from a database
    INSERT INTO - inserts new data into a database
    CREATE DATABASE - creates a new database
    ALTER DATABASE - modifies a database
    CREATE TABLE - creates a new table
    ALTER TABLE - modifies a table
    DROP TABLE - deletes a table
    CREATE INDEX - creates an index (search key)
    DROP INDEX - deletes an index




# Nano Editor and Basic Nano commands 

 *  Shortcut to opening your terminal and launching nano press ctrl+alt+t and type in nano
 * Create a file 
  ```bash
        nano note.txt
  ```
* Typing and saving 
 ```bash
        8 AM-        Lunch
        1 PM-        Tea
        5 PM-        DinnerTo save the above text file press ctrl+o then Enter key and you’re done.   
  ```
* Exiting Nano
 ```bash
       Press ctrl+x and your program exits. 
  ```

* Moving Up and Down 
 ```bash
       Press ctrl+n to move down 
       Press ctrl+p to move up
  ```

* Letter and word traversing
 ```bash
       To move your cursor one word at a time press ctrl+space 
       Reverse of moving back one word at a time is esc+space
       Press – ctrl+e to bring your cursor to the end
       Press – ctrl+a to the beginning of the current line
  ```

* Copy and paste
 ```bash
       ​To select the text; position your cursor press esc+shift+a start selecting till the end of the line
       Then press esc+6 to copy the text
       Position your cursor to last line and press ctrl+u and it’s pasted
       In case you wish to undo the selection thing press the same key combination you did to select text before i.e. esc+shift+a
  ```
* Cut and paste
 ```bash
       ​To cut text do over the “select” thing on the last line and press ctrl+k
       Position your cursor to last line and press ctrl+u and it’s pasted
  ```

* Find words
 ```bash
       You might have noticed this below status: “^W Where is”. If you’ve guessed it correctly it’s the find tool
  ```

* Find and replace
 ```bash
       To find words press esc+r 
       Type in “the word you want found” and press Enter key then type in the replacement text as “replacement”. nano will ask you if you wish to replace that instant of the word Lunch being found
       ​Press y and the word gets replaced.  
  ```


