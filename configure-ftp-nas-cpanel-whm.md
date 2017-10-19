---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-18"
---
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuring FTP for NAS with cPanel & WHM

## Overview

cPanel&WHM can be used with your NAS to upload data via File Transfer Protocol (FTP) to your NAS storage device. Follow the steps below to configure FTP for your NAS with cPanel&WHM. For more information on configuring transfers with cPanel&WHM, refer to cPanel's wiki for [configuration](http://docs.cpanel.net/twiki/bin/view/11_34/WHMDocs/ConfigBackup){:new_window}.

## Configure FTP with cPanel&WHM

|Configuration Option|Entry|
|---|---|
|Backup Type|Remote FTP (Accounts Only)|
|Remote FTP Host|The host name for the NAS storage|
|FTP Backup User|The username associated with the selected NAS|
|FTP Backup Password|The password associated with the selected NAS|

1. Login to WHM using your unique credentials.

2. Select **Configure Backup** from the **Backup** menu option on the **Home** screen.<br/><br/>**Note:** The Configure Backup screen may also be accessed by entering Configure Backup in the Search bar from any screen within WHM.

3. Update the **Configuration Options** based on your backup preferences. Refer to the table below for the required Configuration Option
updates. For information on additional options, refer to cPanel's wiki for [backup configuration](http://docs.cpanel.net/twiki/bin/view/11_34/WHMDocs/ConfigBackup){:new_window}.

4. Click the **Save** button to save the configuration.

5. Run the following script to test the configuration:<br/><br/>`/usr/local/cpanel/scripts/cpbackup`<br/><br/>**Note:** If the configuration was not updated as desired, repeat the steps above to update the configuration.
