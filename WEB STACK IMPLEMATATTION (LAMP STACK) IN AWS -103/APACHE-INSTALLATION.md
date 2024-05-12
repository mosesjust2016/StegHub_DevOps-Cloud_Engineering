## INSTALL APACHE 

* 1. Update a list of packages in package manager 

```bash
sudo apt update 
```

<img src="../images/update-package-manager.PNG" alt="update package manager">

* 2. Install Apache

```bash
 sudo apt install apache2
```

<img src="../images/install-apache.PNG" alt="install apache">


* 3. Verify Apache is running 

```bash
 sudo systemctl status apache2
```

<img src="../images/apache-status.PNG" alt="apache status">

* 4. Access Apache locally

```bash
 curl http://localhost:80
```

<img src="../images/access-local.PNG" alt="loacl access">


* 4. Access Apache locally

```bash
http://<Public-IP-Address>:80
```

<img src="../images/apache-default-page.PNG" alt="apache default page">

* 4. Another way

```bash
curl http://<Public-IP-Address>/latest/meta-data/public-ipv4
```

<img src="../images/apache-another-way.PNG" alt="apache another way">