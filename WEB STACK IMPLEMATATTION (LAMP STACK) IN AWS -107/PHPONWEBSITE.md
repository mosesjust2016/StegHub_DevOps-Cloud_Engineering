## Enable PHP on website

* 1. Change website startup behavior

```bash
 sudo vim /etc/apache2/mods-enabled/dir.conf
```

<img src="../images/virtualhost-directory.PNG" alt="Virtual Host Directory">

* 2. Change website startup behavior

```bash
 <IfModule mod_dir.c>
        # DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        DirectoryIndex index.php index.html index.cgi index.pl  index.xhtml index.htm

</IfModule>
```

<img src="../images/directory-index.PNG" alt="Directory Index">


* 3. Apache Reload

```bash
    sudo systemctl reload apache2
```

<img src="../images/reload-apache.PNG" alt="Reload Apache">


* 4. Create a new file named index.php

```bash
    sudo vim /var/www/projectlamp/index.php
```

<img src="../images/create-index-php.PNG" alt="Create php file">

* 5. Edit index.php

```bash
    sudo vim /var/www/projectlamp/index.php
```

<img src="../images/edit-index-php.PNG" alt="Edit php file">

<img src="../images/index-php-mod.PNG" alt="PHP file">

