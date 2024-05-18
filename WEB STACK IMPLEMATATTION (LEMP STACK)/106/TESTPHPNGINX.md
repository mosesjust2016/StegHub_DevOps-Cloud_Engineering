## TEST PHP NGINX

# Testing PHP with Nginx

* 1. Create Test PHP File

```bash
     nano /var/www/projectLEMP/info.php
```

<img src="../../images/nginx-create-phpinfo.PNG" alt="Create Nginx Info">


* 2. PHP Valid Code

```bash
     <?php 
     phpinfo();
     
```

<img src="../../images/nginx-php-info.PNG" alt="Nginx PHP info">


* 3. Access info.php

```bash
    http://server_domain_or_ip/info.php
     
```

<img src="../../images/info-page.PNG" alt="PHP info">

* . Remove info.php

```bash
    sudo rm /var/www/projectLEMP/info.php
     
```

<img src="../../images/remove-info-php.PNG" alt="Remove PHP info">