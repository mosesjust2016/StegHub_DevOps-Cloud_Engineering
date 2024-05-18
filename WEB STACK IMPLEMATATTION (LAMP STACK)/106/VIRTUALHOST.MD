## CREATE A VIRTUAL HOST FOR YOUR WEBSITE USING APACHE

* 1. Create virtual host directory

```bash
 sudo mkdir /var/www/projectlamp
```

<img src="../../images/virtualhost-directory.PNG" alt="Virtual Host Directory">

* 2. Assign ownership of directory

```bash
 sudo chown -R $USER:$USER /var/www/projectlamp
```

<img src="../images/directory-ownership.PNG" alt="Directory Ownership">


* 3. Create a new configuration file in Apache's sites-available

```bash
 sudo vi /etc/apache2/sites-available/projectlamp.conf
```

<img src="../images/directory-ownership.PNG" alt="Directory Ownership">

* 4. Bare bones Configurarion file 

```bash

 <VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
 </VirtualHost>
```

<img src="../images/insert-virtualhost.PNG" alt="Insert">
<img src="../images/write-quit-virtualhost.PNG" alt="Insert">

* 5. Show New file in sites-available

```bash
 sudo ls /etc/apache2/sites-available
```

<img src="../images/new-config-availablesites.PNG" alt="Directory Ownership">

* 6. Enable new virtual host

```bash
 sudo a2ensite projectlamp
```

<img src="../images/enable-virtualsite.PNG" alt="Enable Virtual Host">

* 7. Run Apache Reload

```bash
 sudo systemctl reload apache2
```

<img src="../images/reload-apache.PNG" alt="Reload Apache">


* 8. Disable Apache default website

```bash
 sudo a2dissite 000-default
```

<img src="../../images/disable-default-website.PNG" alt="Default website">

* 9. Make sure configuration file does not contain syntax error 

```bash
 sudo apache2ctl configtest
```

<img src="../../images/syntax-confirm.PNG" alt="Syntax confirm">

* 10. Run Apache Reload

```bash
 sudo systemctl reload apache2
```

<img src="../../images/reload-apache.PNG" alt="Reload Apache">



* 11. Create index.html

```bash
 sudo vi /var/www/projectlamp/index.html
```

<img src="../../images/insert-index-file.PNG" alt="index.html">


* 12. Edit index.html

```bash
    sudo echo 'Helo LAMP from hostname' $(curl -s http://172.31.18.251/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://172.31.18.251/latest/meta-data/public-ip4) > /var/www/projectlamp/index.html
```

<img src="../../images/index-file-html.PNG" alt="Insert index.html">
