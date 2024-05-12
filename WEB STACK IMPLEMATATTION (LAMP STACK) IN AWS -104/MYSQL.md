## INSTALL MYSQL

* 1. Install MySQL

```bash
 sudo apt install mysql-server
```

<img src="../images/install-mysql.PNG" alt="install mysql">

* 2. Log in to MySQL

```bash
 sudo mysql
```

<img src="../images/mysql-login.PNG" alt="mysql login">


* 3. Run Security Script to remove defaule insecure settings on MySQL

```bash
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```
<img src="../images/alter-mysql.PNG" alt="Alter mysql">

* 4. Exit MySQL

```bash
    mysql> exit
```

<img src="../images/exit-mysql.PNG" alt="Alter mysql">

* 5. Start Interactive script

```bash
    sudo mysql_secure_installation
```

<img src="../images/mysql-interactive01.PNG" alt="Secure install mysql">


* 6. Test if you can login on MySQL console

```bash
    sudo mysql -p 
```

<img src="../images/mysql-test-login.PNG" alt="Login mysql">

* 7. Exit MySQL

```bash
    mysql> exit
```

<img src="../images/exit-mysql.PNG" alt="Exit mysql">

