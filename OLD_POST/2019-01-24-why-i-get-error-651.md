---
layout: post
published: true
title: Why I Get Error 651
categories: Net
tags: Tech
---
## Why i am receiving an Error 651 message? 

This message usually happens when you try to connect to the internet. The error appears and the connection fails, you try to initiate the dialer in Windows 7 and only found that it doesn’t work and returned with an Error 651: Your modem (or other connecting device) has reported an error.  
You had tried to restart your PC, your router, your modem etc. and the problem doesn’t go away.

Error 651 is a Microsoft Windows error code that means the modem, or whatever hardware the computer is using to connect to the internet or a network, is reporting an error. There are a myriad of causes for this error code to appear, but it usually results from a driver error or failure of the modem. Because there are so many causes to this problem, there is no universal solution, but there are a few steps that solve the majority of known causes. Allow Windows to troubleshoot the problem itself first by running the network troubleshooter and following its suggestions. In most cases, if the troubleshooter can not provide you with the solution, it will usually give you valuable information such as the status of certain hardware and software, and possibly save you time and effort.

## What causes the Error 651 ?

*   The raspppoe.sys file has become corrupted. RASPPPOE.sys is an acronym for Remote Access Service Point-to-Point Protocol over Ethernet. This is a windows driver that many broadband service providers use for authentication when connecting to the internet through a broadband modem.
*   Possible problems with the Local Area Network (LAN) card driver.
*   There may be a conflict with the modem driver and your operating system.

## How to resolve this problem ?

*   Try rebooting your computer. Sometimes a simple reboot will clear your cache and reset the modem.
*   Rename the existing RASPPPOE.sys file and take a copy of the file from a Windows Vista system. Apparently this problem has been reported for Windows 7 users, by renaming the current file and copying this file from Windows Vista, it should resolve the issue. This file can be found in c:\\windows\\system32\\drivers.
*   Re-install LAN Driver. It’s also possible that your drivers are outdated and you may need to download updates from the manufacturer’s website.
*   Install the latest patches for your current Windows OS.

It’s possible that there is a conflict between your OS and your driver. Or there is a corrupt file in your system registry. This could be done manually if you knew what file to adjust. Not highly recommended for the risk it poses of causing a complete system failure. Another possibility is to run a registry cleaner.

This system tool will seek out any invalid or corrupted files in your registry and make necessary fixes as needed. It will also fix any driver errors and add any missing system files needed for optimal performance.
