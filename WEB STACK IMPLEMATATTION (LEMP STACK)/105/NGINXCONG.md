## CONFIGURE NGINX

# Configuring Nginx to use PHP Processor

* 1. Create a web directory for your domain

```bash
     sudo mkdir /var/www/projectLEMP
```

<img src="../../images/nginx-lemp-config.PNG" alt="Nginx Configuration">

* 2. Assign ownership of directory

```bash
 sudo chown -R $USER:$USER /var/www/projectLEMP
```

<img src="../../images/nginx-lemp-dir-owner.PNG" alt="Directory Ownership">


* 3. Install Nano

```bash
 sudo apt install nano
```

<img src="../../images/install-nano.PNG" alt="Install Nano">


* 4. Create a new configuration file

```bash
 sudo nano /etc/nginx/sites-available/projectLEMP
```
<img src="../images/directory-ownership.PNG" alt="Directory Ownership">


* 5. Create a new configuration file

```bash
#/etc/nginx/sites-available/projectLEMP

server {
    listen 80;
    server_name projectLEMP www.projectLEMP;

    root /var/www/projectLEMP;

    index index.html index.htm index.php;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
   }

    location ~ /\.ht {
        deny all;
    }
}
```

<img src="../../images/nginx-php-config-file.PNG" alt="Nginx Configuration File">

* 6. Activate new configuration file

```bash
 sudo ln -s /etc/nginx/sites-available/projectLEMP /etc/nginx/sites-enabled/
```

<img src="../../images/nginx-activate-config.PNG" alt="Activate Nginx">

* 7. Test for syntax errors

```bash
 sudo nginx -t
```

<img src="../../images/nginx-syntax-test.PNG" alt="Test Syntax Nginx">

* 8. Disable Default Nginx host

```bash
 sudo unlink /etc/nginx/sites-enabled/default
```

<img src="../../images/unlink-default-nginx.PNG" alt="Unlink Default Nginx">


* 8. Reaload Nginx 

```bash
 sudo systemctl reload nginx
```

<img src="../../images/nginx-reload.PNG" alt="Reload Nginx">


* 8. Create index.html 

```bash
 sudo nano /var/www/projectLEMP/index.html
```

<img src="../../images/create-index-lemp.PNG" alt="Create Index">

* 9. Edit index.html 

```bash
    sudo echo 'Helo LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ip4) > /var/www/projectLEMP/index.html
```

<img src="../../images/create-index-lemp.PNG" alt="Create Index">

* 10. Access index.html using IP address

```bash
    http://<PUBLIC IP Address>:80
```

<img src="../../images/lemp-index-html.PNG" alt="Index">


* 11. Access index.html using IP address

```bash
    http://<PUBLIC DNS Name>:80
```






