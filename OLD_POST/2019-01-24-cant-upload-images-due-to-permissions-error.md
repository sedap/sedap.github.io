---
layout: post
published: true
title: Can’t upload images due to permissions error
categories: Net
tags: Tech
---
For some reason when I try to upload an image to my blog I get an error message saying that WP can’t create a folder under the relevant directory (wp-content/uploads/2018/09) and it’s asking if the folder above it has write permissions. The parent folder indeed has write permissions. I tried creating the folder manually and it still shows the same error message.  

This error happens when PHP (WordPress) can’t write to the file. This is caused by not having write permissions or the username or group that PHP (WordPress) is running under doesn’t have permission to write to the file.

755 permissions will allow WordPress write permissions when PHP is running as the username under most shared host plans.

Some FTP programs will allow you to change the user and group assigned to the folders. You can also make this change using Cpanel’s file manager.

The folders should have the same username as your Cpanel account.

Some server environments require you to use 777 permissions for PHP to have write access. This is not secure in a shared hosting environment. You can change your permissions to 777 temporarily to see if that allows you to upload photos but **MAKE SURE YOU CHANGE THEM BACK TO 755 WHEN YOUR DONE.**

Your hosting provider should also be able to provide help in this situation.
