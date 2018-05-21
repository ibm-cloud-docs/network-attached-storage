---
copyright:
  years: 1994, 2018
lastupdated: "2018-05-21"
---
{:shortdesc: .shortdesc}
{:note: .deprecated}
{:new_window: target="_blank"}

# Connecting to NAS Storage in Windows

## Overview

You can map NAS storage in Windows either in the command line or through point-and-click interaction in the File Explorer.

## Connect to NAS Storage

|To connect to the NAS through…|Then…|
|---|---|
|The Command Line|Enter the **command** below in the Command Line.  No further action is required to map the NAS.<br/><br/><code>net use {drive letter}: \\Hostname\Username /u:username password</code><br/><br/>**Example:**<blockquote>net use z: \\nas0X.service.softlayer.com\auser /u:auser apass</blockquote>|
|Windows File Explorer|Proceed to the next step.|

1. Determine if you want to connect to NAS storage through the command line or through Windows File Explorer.

2. From the **Tools** menu for the server, slect **Map Network Drive**.

3. Select the **Drive Letter** you want from the **Drive** list.

4. Enter the path to the NAS in the **Folder** field in the following format:<br/><br/>
```
\\nas0X.service.softlayer.com\{NASusername}
```

5. Select **Connect Using a Different User Name**  and enter the following information:
  * Enter the NAS User name in the **Username** field.
  * Enter the NAS password in the **Password** field.

6. Select the **Reconnect on Login** check box to automatically reconnect to the NAS on login.

7. Click **Finish**.
