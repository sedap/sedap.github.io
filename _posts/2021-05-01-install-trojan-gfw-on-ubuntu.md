---
layout: post
published: true
title: Install Trojan-GFW on Ubuntu Linux
categories: Net
tags: [trojan, trojan-gfw, tunnel, ubuntu, debian]
description: >-
  How to quickly install trojan-gfw on ubuntu or debian linux
---



Here I summarize a short and quick way to install n

The operating system I use is Ubuntu 20.04 but it can also be used on Debian.

```bash
sudo su
apt update
```


install nginx web server
```bash
apt install nginx
```

Configure nginx
edit file _/etc/nginx/sites-available/default_
```bash
vi /etc/nginx/sites-available/default
```

replace _ in line **_server_name _;_**  with your domain name; e.g. _hahahaha.com_

copy default  file _index.nginx-debian.html_ to _index.html_
```bash
cp /var/www/html/index.nginx-debian.html /var/www/html/index.html
```

run nginx server

```bash
systemctl start nginx
```

check if nginx server is running well, use browser or curl
```bash
curl hahahaha.com
```

install and configure certbot
```bash
apt install certbot python3-certbot-nginx
```

configure certybot
```bash
certbot certonly --nginx
```
enter email address and accept licence

on part : Which names would you like to activate HTTPS for?

enter the server number that will be given the certificate

then the certificates will be stored in _/etc/letsencrypt/live/hahahaha.com/_

```bash
ls -la /etc/letsencrypt/live/hahahaha.com/
```

fix the file permissions 
```bash
chmod +rx /etc/letsencrypt/live
chmod +rx /etc/letsencrypt/archive
chmod -R +r /etc/letsencrypt/archive/hahahaha.com
```

install trojan
```bash
apt install trojan
```

configure trojan
edit file config.json
```bash
vi /etc/trojan/config.json
```

delete _password1_ 

replace _password2_ with the desired password, for example _123_

edit the cert section, replace the contents with the certificate from certbot
```bash
"cert": "/path/to/certificate.crt",
"key": "/path/to/private.key",
```
become
```bash
"cert": "/etc/letsencrypt/live/hahahaha.com/fullchain.pem",
"key": "/etc/letsencrypt/live/hahahaha.com/privkey.pem",
```

enable trojan service
```bash
systemctl enable trojan
```

run trojan service
```bash
systemctl start trojan
```
check trojan service status see if there is an error.
```bash
systemctl status trojan
```


check service status, trojan on port 443 and nginx on port 80
```bash
ss -tulpn
```
.
