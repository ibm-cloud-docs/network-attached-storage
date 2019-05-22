---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

keywords: NAS, FreeBSD

subcollection: network-attached-storage

---
{:deprecated: .deprecated}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}
{:external: target="_blank" .external}
{:external: target="_blank" .external}
{:pre: .pre}
{:tip: .tip}

# Mounting NAS Storage in FreeBSD
{: #mountNASFreeBSD}

All instances of this service are deprecated. For more information, contact [sales or support](https://www.ibm.com/cloud-computing/bluemix/contact-us).
{:deprecated}

Mounting your NAS Storage to a device that runs on FreeBSD can be done by using a series of simple commands in the command line.

1. Create a folder with the following command.
   ```
   mkdir /local/mountpoint
   ```

2. Run the following command to mount the NAS.
   ```
   mount_smbfs -I NASIP //username@NASIP/username /local/mountpoint
   ```

3. Enter the NAS password when you are prompted.

   **Example**

   ```
   [root@freebsdnastest ~]# mkdir /mnt/nas
   [root@freebsdnastest ~]# mount_smbfs -I 10.0.78.87 //SL12345-1@10.0.78.87/SL12345-1 /mnt/nas
   Password:
   [root@freebsdnastest ~]#
   ```

4. Set the NAS to mount on reboot with the following steps.

   - Add the following command to the `/etc/fstab` file.
     ```
     //username@NASIP/username /local/mountpoint smbfs rw,-N,-INASIP 0 0
     ```

     **Example `/etc/fstab` output**
     ```
     [root@freebsdnastest ~]# cat /etc/fstab
     /dev/ada0p2     /           ufs rw 1 1
     /dev/ada0p3     none       swap sw 0 0
     /dev/ada0p4     /tmp        ufs rw 2 2
     /dev/ada0p5     /var        ufs rw 2 2
     /dev/ada0p6     /usr        ufs rw 2 2
     //SL12345-1@10.0.78.87/SL12345-1 /mnt/nas smbfs rw,-N,-I10.0.78.87 0 0
     ```

   - Add the NAS user name and password to `/etc/nsmb.conf`.
     ```
     [SERVERNAME:MYUSER]
     password=myPassword
     ```

     **Example**
     ```
     [root@freebsdnastest ~]# cat /etc/nsmb.conf
     [10.0.78.87:SL12345-1]
     password=NASPASSWORD
     ```

5. Unmount and mount the NAS to verify that it is configured properly.
   1. Unmount the storage.

      ```
      [root@freebsdnastest ~]# df -Th /mnt/nas/
      Filesystem   Type    Size    Used   Avail Capacity  Mounted on
      /dev/ada0p2  ufs       1G    624M    302M    67%    /  
      ```

   2. Mount the storage.

      ```
      root@freebsdnastest ~]# df -Th /mnt/nas/
      Filesystem                          Type     Size    Used   Avail Capacity  Mounted on
      //SL179555-1@10.0.78.87/SL179555-1  smbfs      2T    1.0T    993G    51%    /mnt/nas
      ```
