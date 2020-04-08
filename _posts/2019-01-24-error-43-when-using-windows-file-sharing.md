---
layout: post
published: true
title: Error-43 When Using Windows File Sharing
categories: Internet
tags: Tech
---
On Mac OS X, when you connect to the Windows share, or when try to copy files to/from it, you see an alert box with a message similar to this one:

The operation cannot be completed because one or more required items cannot be found. (Error code = -43).

There are three causes for this:

*   Illegal characters.
*   A permissions issue
*   A non-existent share point.

**Illegal characters**

This occurs because Mac OS X allows you to use certain characters in file names that Microsoft Windows operating systems do not allow. The alert message text does not make this clear and may be regarded as erroneous. If you frequently share files with Windows computers, you may wish to follow naming protocols for the version of Windows that is in use.

These are the characters not allowed:

? \[ \] / \\ = + < > ; : ” , | \*

Respectively, these are the question mark, left and right brackets, solidus (or “forward slash”), reverse solidus (or “backslash”), equals sign, plus sign, left and right angle brackets, semicolon, colon, quotation mark, comma, pipe, and asterisk.

If the issue occurs when you are trying to open or copy a file, remove these characters from the file names.

If this issue occurs when you are connecting to the SMB server, it may be because the share name contains the illegal character. Be sure to avoid the illegal characters in the names of shares, folders, or drives.

When this is caused by illegal characters on the server, note that users of Windows operating systems will get the same -43 error message.

**Permissions**

Generally speaking, this could happen if connecting to any SMB server via a URL that contains the name of a share point for which the connecting user does not have adequate permissions, such as:

**SMB://myNetbiosComputerName/restricted\_share**

You can avoid this issue by using the URL of the server only, without the share name, such as:

**SMB://myNetbiosComputerName**

After you connect, you will be prompted to choose from share points to which you have access.

If the SMB server is a Mac OS X Server version 10.2 to 10.2.8, then any folders enclosing the SMB share point must have at least read-only or execute permissions set for the user or group that is connecting. You may use Workgroup Manager to set read-only access for the enclosing folder(s). Alternatively, advanced users may use the chmod command to set execute privileges for the enclosing folders.  

**Non-existent share point**

You may get the -43 message if try to connect using a URL that contains the name of a share point that does not exist. As in the example above, you may simply omit the share point name from the server’s URL, then follow the prompts to select your share point.
