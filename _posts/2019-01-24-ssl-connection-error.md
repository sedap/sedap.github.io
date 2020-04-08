---
layout: post
published: true
title: SSL Connection Error
categories: Internet
tags: Tech
---
I can’t access Google and Gmail on any browsers and there’s a message stating SSL Connection Error:107

Error Message when I try to load gmail.com or Google Calendar:  
SSL connection error.

Unable to make a secure connection to the server. This may be a problem with the server, or it may be requiring a client authentication certificate that you don’t have.

Error 128 (net::ERR\_SSL\_UNSAFE\_NEGOTIATION): The SSL renegotiation extension was missing from the secure handshake. For some sites, which are known to support the renegotiation extension, Chrome requires a more secure handshake to prevent a class of known attacks. The omission of this extension suggests that your connection was intercepted and manipulated in transit.

If you’re using Internet Explorer: At the top go to Tools then Internet Options, then click on the tab that says Advanced. Scroll down through the list and you want to make sure that “Use SSL 3.0″ is checked.

If you’re using Firefox: At the top go to Tools, then Options. Then the tab that says Advanced. Click on the tab in the lower portion that says Encryption. Make sure “Use SSL 3.0″ is selected.

If you’re using Google Chrome: Uninstall and reinstall the newest version.
