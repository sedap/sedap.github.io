---
layout: post
<<<<<<< HEAD
published: true
title: Install Trojan-GFW on Ubuntu Linux
categories: Net
tags: Tech
description: >-
  How to quickly install trojan-gfw on ubuntu or debian linux
---



Here I summarize a short and quick way to install [Trojan-GFW] (https://github.com/trojan-gfw/trojan) on Ubuntu Linux.

The operating system I use is Ubuntu 20.04 but it can also be used on Debian.

```bash
sudo su
apt update
```

# install nginx web server

```bash
apt install nginx
```

# Configure nginx
# edit /etc/nginx/sites-available/default

```bash
vi /etc/nginx/sites-available/default
```

# replace _ in line "server_name _;"  with your domain name; e.g. hahahaha.com
# copy default index.nginx-debian.html to index.html
mv /var/www/html/index.nginx-debian.html /var/www/html/index.html
# run nginx server
systemctl start nginx

#check if nginx server is running well, use browser or curl
curl hahahaha.com



#install and configure certbot
apt install certbot python3-certbot-nginx

certbot certonly --nginx
#enter email address and accept licence

#on part : Which names would you like to activate HTTPS for?
#masukkan nomor server yg anak di bei sertifikat
#sertifkat tersimpan di /etc/letsencrypt/live/hahahaha.com/
ls -la /etc/letsencrypt/live/books.meetmath.com/
#perbaiki permission file nya
chmod +rx /etc/letsencrypt/live
chmod +rx /etc/letsencrypt/archive
chmod -R +r /etc/letsencrypt/archive/hahahaha.com


#install trojan
apt install trojan

#configure trojan
#edit file vi config.json
vi /etc/trojan/config.json
#hapus password1, 
ganti password2 dengan password untuk yang diinginkan misalnya 123
# edit bagian cert, ganti isinya dengan certifikat dari certbot
#"cert": "/path/to/certificate.crt",
#"key": "/path/to/private.key",
menjadi
"cert": "/etc/letsencrypt/live/hahahaha.com/fullchain.pem",
"key": "/etc/letsencrypt/live/hahahaha.com/privkey.pem",

#enable trojan service
systemctl enable trojan

#run trojan service
systemctl start trojan

#check trojan service status lihat apakah ada yang error.
systemctl status trojan


#cek status service, trojan di port 443 dan nginx di port 80
ss -tulpn





#install speed test cli
curl -s https://install.speedtest.net/app/cli/install.deb.sh | sudo bash
sudo apt-get install speedtest



If you find that your WhatsApp suddenly has an error with code 910, try the following steps to resolve it

1. Remove your Google account by going to your phone's Settings. Then tap Users & accounts.
2. Select your Google account and tap **_Remove Account > Remove Account_**.
3. Restart your phone or turn it off and on.
4. Re-add your Google account by going to your phone's Settings. Then tap **Users & accounts > Add account > Google._**
5. Log in to your Google account.
6. Clear Google Play Store's cache by going to your phone's Settings. Then tap **_Apps & notifications > App info > Google Play Store > Storage > CLEAR CACHE_**.
7. Clear Google Play Store's data by tapping **_CLEAR DATA > OK_**.
8. Try downloading WhatsApp again.

The steps above can also be used to resolve whatsapp errors with codes 413, 491, 492, 505, 907, 921, 927, 941 and DF-DLA-15


## As for error codes 101, 498 and 919, here are the steps you can try to do

1. Go to your phone's Settings, then tap **_Apps & notifications > App info > Google Play Store > Storage > CLEAR CACHE._**
2. Tap **_CLEAR DATA > OK_**.
3. Restart your phone, then try installing WhatsApp again

If you're still unable to install WhatsApp, here are some tips on how to create free space on your phone:
- Clear cache and data by going to your phone's **_Settings > Storage_**.
- Move data and apps to your external SD card.
- Delete apps you're no longer using.
- Look into these hidden WhatsApp folders below. Note you can only access these folders with a file manager:
  1. The folder for photos is located in: _/WhatsApp/Media/WhatsApp Images/Sent_.
  2. The folder for videos is located in: _/WhatsApp/Media/WhatsApp Video/Sent_.
  3. The folder for voice messages is located in: _/WhatsApp/Media/WhatsApp Voice Notes_.
  
  **Note**: If you delete your WhatsApp photos, videos or voice messages, you won't be able to view or listen to them anymore.
  
  
## For error codes: 403, 495, 504, 911, 920, 923, RPC errors, invalid package file, installation or download unsuccessful errors

1. Follow the instructions in the section "There's insufficient space on the device" to make sure you have 2. enough space on your device.
3. Tap this link from our website to download WhatsApp as an APK file.
4. Tap **_DOWNLOAD NOW_**.
5. Open the APK file to initiate the installation.
   **Note**: When opening the APK file, you'll need to tap **_SETTINGS > Allow from this source_**.
   
   
## For error This item isn’t available in your country
If you see a "**_Not available in your country_**" error, or if the Google Play Help Center troubleshooting tips don't help, visit [this page](https://www.whatsapp.com/android "Download Whatsapp APK") to download WhatsApp as an APK file and update the app. When opening the APK file, you'll need to tap **_SETTINGS > Allow_** from this source.