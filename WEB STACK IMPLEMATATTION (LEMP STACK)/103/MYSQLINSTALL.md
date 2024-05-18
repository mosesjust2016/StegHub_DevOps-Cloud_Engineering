## NGINX

# INSTALL MYSQL

* 1. Installing MySQL

```bash
    sudo apt install mysql-server
```

<img src="../../images/nginx-mysql-install.PNG" alt="Mysql Install">

* 2. Log in to the MySQL Console

```bash
    sudo mysql
```

<img src="../../images/nginx-mysql-console.PNG" alt="Mysql Console">

* 3. Run security script

```bash
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```

<img src="../../images/nginx-mysql-security-script.PNG" alt="Mysql Security Script">

* 4. Exit MySQL

```bash
    mysql> exit
```

<img src="../../images/nginx-mysql-exit.PNG" alt="Exit mysql">

* 5. Start Interactive script

```bash
    sudo mysql_secure_installation
```

<img src="../../images/nginx-mysql-secure-install.PNG" alt="Secure install mysql">

* 6. Test if you can login on MySQL console

```bash
    sudo mysql -p 
```

<img src="../../images/nginx-mysql-login.PNG" alt="Login mysql">

* 7. Exit MySQL

```bash
    mysql> exit
```

<img src="../../images/nginx-mysql-exit.PNG" alt="Exit mysql">