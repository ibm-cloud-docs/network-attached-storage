---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-18"
---
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mounting NAS Storage in Linux

## Overview

Mounting your NAS Storage to a device that runs on a Linux-based Operating System can be done using a series of simple commands in the shell or terminal within the OS.  This procedure outlines the steps required to mount NAS Storage on any of the following operating systems:

* RedHat Enterprise Linux
* CentOS
* CloudLinux
* Debian
* Ubuntu

Please note that while the majority of steps apply to all of the operating systems listed above, the commands required to determine if your CIFS utility is installed on Debian and Ubuntu are unique.  Follow the steps below to mount NAS Storage to your Linux-based OS.

## Mount NAS Storage

1. Determine if the OS on your device is RedHat Enterprise Linux, CentOS or CloudLinux -OR- Debian or Ubuntu.

  |If your device is running…|Then…|
  |---|---|
  |RedHat Enterprise Linux, CentOS or CloudLinux|Determine if the cifs-utils utility is installed by running the following command:<blockquote>root@slnastest [~]# rpm -q cifs-utils<br/><br/>**Note:** If cifs-utils is not installed, the following message will appear:<blockquote>package cifs-utils is  not installed</blockquote><ul><li>If cifs-utils is installed, proceed to the next step.</li><li>If cifs-utils is not installed, install the utility using the following command:<blockquote>root@slnastest [~]# yum install cifs-utils</blockquote></li></ul>|
  |Debian or Ubuntu|Determine if the cifs-utils utility is installed by running the following command:<blockquote>root@slnastest:~# dpkg-query -S cifs-utils<br/><br/>**Note:** If cifs-utils is not installed, the following message will appear:<blockquote>dpkg-query: no path found matching   pattern *cifs-utils*.</blockquote><ul><li>If cifs-utils is installed, proceed to the next step.</li><li>If cifs-utils is not installed, install the utility using the following command:<blockquote>`root@slnastest [~]# apt-get install cifs-utils`<br/>`root@slnastest:~# dpkg-query -S cifs-utils`<br/>`cifs-utils: /usr/share/doc/cifs-utils`<br/>`cifs-utils: /usr/share/doc/cifs-utils/changelog.gz`<br/>`cifs-utils: /usr/share/doc/cifs-utils/NEWS.Debian.gz`<br/>`cifs-utils: /usr/share/doc/cifs-utils/changelog.Debian.gz`<br/>`cifs-utils: /usr/share/doc/cifs-utils/copyright`</blockquote></li></ul>|

2. Create the directory and mount the device using the following commands:
   ```
   mkdir /local/mountpoint
   mount -t cifs //Hostname/Username -o username=username,password=password,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt
   ```
   **Example:**
   ```
   root@slnastest [~]# mkdir /mnt/nas
   root@slnastest [~]# mount -t cifs //nas05.service.softlayer.com/SL12345-1 -o username=SL12345-1,password=NASPASSWORD,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nas
   root@slnastest [~]# df -Th /mnt/nas/
   Filesystem                              Type    Size  Used Avail Use% Mounted on
   //nas05.service.softlayer.com/SL12345-1 cifs     54T   49T  5.3T  91% /mnt/nas
   ```

3. Determine if the NAS should mount on reboot.
