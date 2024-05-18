## NGINX

# INSTALL NGINX

* 1. Installing nginx web server

```bash
    sudo apt update
    sudo apt install nginx
```

<img src="../../images/nginx-apt-update.PNG" alt="Apt Update">
<img src="../../images/nginx install.PNG" alt="Nginx Install ">

* 2. Nginx Status

```bash
    sudo systemctl status nginx
```

<img src="../../images/nginx-status.PNG" alt="Nginx Status">


* 3. Access Nginx locally

```bash
    curl http://localhost:80
    or 
    curl http://127.0.0.1:80
```

<img src="../../images/nginx-loacl-access.PNG" alt="Nginx Local Access">

* 4. Access Nginx using IP Address

```bash
    curl http://<PUBLIC IP>:80
   
```

<img src="../../images/nginx-ip-access.PNG" alt="Nginx IP Access">


* 4. Getting your Public IP Address

```bash
    curl -s http://169.254.169.254/latest/meta-data/public-ipv4
   
```

<img src="../../images/my-public-ip.PNG" alt="My PUBLIC IP">