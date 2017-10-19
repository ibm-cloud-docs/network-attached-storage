---
copyright:
  years: 1994, 2017
lastupdated: "2017-10-18"
---
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Mounting NAS Storage in FreeBSD

## Overview

Mounting your NAS Storage to a device that runs on FreeBSD can be done using a series of simple commands in the command line.  Follow the steps below to mount NAS storage in FreeBSD.

## Mount NAS Storage

1. Create a folder in FreeBSD that will be used to mount NAS with the following command:

          mkdir /local/mountpoint

2. Run the following command to mount the NAS:

        mount_smbfs -I NASIP //username@NASIP/username /local/mountpoint

3. Enter the NAS Password in the appropriate location in the command line when prompted.<br/><br/>**Example:**

          [root@freebsdnastest ~]# mkdir /mnt/nas
          [root@freebsdnastest ~]# mount_smbfs -I 10.0.78.87 //SL12345-1@10.0.78.87/SL12345-1 /mnt/nas
        Password:
          [root@freebsdnastest ~]#

4. Set the NAS to mount on reboot with the following steps:

   * Add the following **command** to the `/etc/fstab` file:<br/><br/>`//username@NASIP/username /local/mountpoint smbfs rw,-N,-INASIP 0 0`<br/><br/>**Example `/etc/fstab` output:**

        [root@freebsdnastest ~]# cat /etc/fstab
        /dev/ada0p2     /           ufs rw 1 1
        /dev/ada0p3     none       swap sw 0 0
        /dev/ada0p4     /tmp        ufs rw 2 2
        /dev/ada0p5     /var        ufs rw 2 2
        /dev/ada0p6     /usr        ufs rw 2 2
        //SL12345-1@10.0.78.87/SL12345-1 /mnt/nas smbfs rw,-N,-I10.0.78.87 0 0

   * Add the **NAS username and password** to `/etc/nsmb.conf`:

        [SERVERNAME:MYUSER]
        password=myPassword

    **Example:**

            [root@freebsdnastest ~]# cat /etc/nsmb.conf
            [10.0.78.87:SL12345-1]
        password=NASPASSWORD

5. Unmount and mount the NAS to verify that it has been configured properly.  Refer to the table below for the unmount and mount commands.

|Action|Command|
|---|---|
|Unmount the NAS|`[root@freebsdnastest ~]# umount /mnt/nas/`<br/>`[root@freebsdnastest ~]# df -Th /mnt/nas/`<br/>`Filesystem   Type    Size    Used   Avail Capacity  Mounted on`<br/>`/dev/ada0p2  ufs       1G    624M    302M    67%    /`|
|Mount the NAS|`[root@freebsdnastest ~]# mount /mnt/nas/`<br/>`[root@freebsdnastest ~]# df -Th /mnt/nas/`<br/>`Filesystem                          Type     Size    Used   Avail Capacity  Mounted on`<br/>`//SL179555-1@10.0.78.87/SL179555-1  smbfs      2T    1.0T    993G    51%    /mnt/nas`|
