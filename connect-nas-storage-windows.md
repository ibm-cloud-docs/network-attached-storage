---
copyright:
  years: 1994, 2018
lastupdated: "2018-03-01"
---
{:shortdesc: .shortdesc}
{:note: .deprecated}
{:new_window: target="_blank"}

# Connecting to NAS Storage in Windows

## Overview

Mapping NAS Storage in Windows may take place either in the Command Line or through point-and-click interaction in the File Explorer.  Complete the steps below to map NAS Storage in Windows.

## Connect to NAS Storage

|To connect to the NAS through…|Then…|
|---|---|
|The Command Line|Enter the **command** below in the Command Line.  No further action is required to map the NAS.<br/><br/>net use {drive letter}: \\Hostname\Username /u:username password<br/><br/>**Example:**<blockquote>net use z: \\nas0X.service.softlayer.com\auser /u:auser apass</blockquote>|
|Windows File Explorer|Proceed to the next step.|

1. Determine if you wish to connect to NAS storage through the Command Line or through Windows File Explorer.

2. Select **Map Network Drive** from the **Tools** menu for the Server.

3. Select the desired **Drive Letter** from the **Drive** drop down list.

4. Enter the path to the NAS in the **Folder** field in the following format:<br/><br/>```\\nas0X.service.softlayer.com\{NASusername}```
5. Select the **Connect Using a Different User Name** option and enter the following information:
  * Enter the **NAS Username** in the **Username** field.
  * Enter the **NAS Password** in the **Password** field.

6. Select the **Reconnect on Login** check box to automatically reconnect to the NAS on login, if desired.

7. Click the **Finish** button.
