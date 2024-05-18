## 107- MYSQL DATABSE WITH PHP

# Retrieving data from MYSQL database with PHP 

* 1. Connect to the MySQL console using root account 

```bash
     sudo mysql -u root -p
```

<img src="../../images/msql-login-password.PNG" alt="Mysql Login">


* 2. Create new database 

```bash
    CREATE DATABASE example_database;
```

<img src="../../images/create-example-db.PNG" alt="Create Example DB">

* 3. Create new user 

```bash
    CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY PassWord.1';
```

<img src="../../images/create-example-user.PNG" alt="Create Example User">

* 4. Grant permissions to new user 

```bash
    GRANT ALL ON example_database.* TO 'example_user'@'%';

```

<img src="../../images/grant-all.PNG" alt="Grant All OnMysql">

* 5. Exit

```bash
    mysql> exit;

```

<img src="../../images/exit-db-nginx.PNG" alt="Exit Mysql">

* 6. Connect to the MySQL console using root account 

```bash
     sudo mysql -u example_user -p
```

<img src="../../images/login-example-db.PNG" alt="Mysql Login">

* 7. Show Databases

```bash
     mysql> SHOW DATABASES;
```

<img src="../../images/show-dbs.PNG" alt="Show DB">


* 7. Create todo_list table 

```bash
    mysql> CREATE TABLE example_database.todo_list (
    ->     item_id INT AUTO_INCREMENT PRIMARY KEY,
    ->     content VARCHAR(255)
    -> );

```

<img src="../../images/create-example table.PNG" alt="Create Example table">
<img src="../../images/show-tables.PNG" alt="Show Example table">


* 7. Insert a few rows 

```bash
    mysql> INSERT INTO example_database.todo_list (content) VALUES ("My first important item");
    mysql> INSERT INTO example_database.todo_list (content) VALUES ("My Second important item");
    mysql> INSERT INTO example_database.todo_list (content) VALUES ("My Third important item");
    mysql> INSERT INTO example_database.todo_list (content) VALUES ("and this one more thing");

```

<img src="../../images/insert-to-table.PNG" alt="Insert into table">

* 7. Display inserted rows

```bash
    mysql> SELECT * FROM example_database.todo_list;
    
```

<img src="../../images/select-todo_list.PNG" alt="Select Todo_list">

* 8. Exit

```bash
    mysql> exit;

```

<img src="../../images/exit-db-nginx.PNG" alt="Exit Mysql">


* 9. Exit

```bash
    nano /var/www/projectLEMP/todo_list.php

```

<img src="../../images/exit-db-nginx.PNG" alt="Exit Mysql">

 
 
* 10. Exit

```bash
    <?php

        // Database credentials
        $server = "localhost";
        $user = "example_user";
        $password = "PassWord.1";
        $database = "example_database";
        $table = "todo_list";

        try {
            $db = new PDO("mysql:host=$server;dbname=$database", $user, $password);
            echo "<h2>TODO</h2><ol>";
            foreach ($db->query("SELECT content FROM $table") as $row) {
                echo "<li>" . $row['content'] . "</li>";
            }
            echo "</ol>";
        } catch (PDOException $e) {
            print "Error!: " . $e->getMessage() . "<br/>";
            die();
        }

```
<img src="../../images/edit-todo_list.PNG" alt="Edit todolist">

 * 11. Access info.php

```bash
    http://Public_domain_or_IP/todo_list.php
     
```

<img src="../../images/todo-page.PNG" alt="PHP info">