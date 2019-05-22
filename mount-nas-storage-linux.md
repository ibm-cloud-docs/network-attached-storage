---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

keywords: NAS, Linux

subcollection: network-attached-storage

---
{:deprecated: .deprecated}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}
{:external: target="_blank" .external}
{:external: target="_blank" .external}
{:pre: .pre}
{:tip: .tip}

# Mounting NAS Storage in Linux
{: #mountNASLinux}

All instances of this service are deprecated. For more information, contact [sales or support](https://www.ibm.com/cloud-computing/bluemix/contact-us).
{:deprecated}

Mounting your NAS Storage to a device that runs on a Linux-based Operating System can be done by using a series of simple commands in the shell or terminal within the OS. You can use these steps to mount NAS Storage on any of the following operating systems:

* RHEL
* CentOS
* CloudLinux
* Debian
* Ubuntu

Linux is a registered trademark of Linus Torvalds in the United States, other countries, or both.
{:tip}

Most of the steps apply to all of the listed Linux operating systems. However, the commands that are required to determine whether the CIFS utility is installed on Debian and Ubuntu are unique. Select the steps that are appropriate for the device's current OS.

## Mounting NAS storage

1. Determine whether the OS on the device is RHEL, CentOS, or CloudLinux **OR** Debian or Ubuntu.
   - If the OS is RHEL, CentOS or CloudLinux, determine whether the <code>cifs-utils</code> utility is installed.
     ```
     root@sllockboxtest [~]# rpm -q cifs-utils
     ```
     {:pre}

       - If `cifs-utils` is installed, proceed to the next step.
       - If `cifs-utils` is not installed, install the utility with the following command.
         ```
         yum install cifs-utils
         ```
         {:pre}

   - If the OS is Debian or Ubuntu, determine whether the `cifs-utils` utility is installed.
     ```
     root@sllockboxtest:~# dpkg-query -S cifs-utils
     ```
     {:pre}

       - If `cifs-utils` is installed, the following message appears: `dpkg-query-S cifs-utils`. Proceed to the next step.
       - If `cifs-utils` is not installed, the following message appears:`dpkg-query: no path found matching pattern *cifs-utils*`. Install the utility by running the following command.
         ```
         apt-get install cifs-utils
         ```
         {:pre}

          ```
          root@sllockboxtest:~# dpkg-query -S cifs-utils
          cifs-utils: /usr/share/doc/cifs-utils
          cifs-utils: /usr/share/doc/cifs-utils/changelog.gz
          cifs-utils: /usr/share/doc/cifs-utils/NEWS.Debian.gz
          cifs-utils: /usr/share/doc/cifs-utils/changelog.Debian.gz
          cifs-utils: /usr/share/doc/cifs-utils/copyright
          ```
2. Create the directory and mount the device.

   ```
   mkdir /local/mountpoint
   mount -t cifs //Hostname/Username -o username=username,password=password /local/mountpoint
   ```
   {:pre}

   **Example**

   ```
   root@slnastest [~]# mkdir /mnt/nas
   root@slnastest [~]# mount -t cifs //nas05.service.softlayer.com/SL12345-1 -o username=SL123451,password=NASPASSWORD,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755,sec=ntlmssp /mnt/nas
   root@slnastest [~]# df -Th /mnt/nas/
   Filesystem                              Type    Size  Used Avail Use% Mounted on
   //nas05.service.softlayer.com/SL12345-1 cifs     54T   49T  5.3T  91% /mnt/nas
   ```

3. Determine whether the storage is to be mounted on restart.
   - If you want the NAS to be mounted on restart, update the `/etc/fstab` file. Replace `SL12345-1` and `NASPASSWORD` with your credentials.

     ```
     \//nas05.service.softlayer.com/SL12345-1        
     /mnt/nas       
     cifs defaults,username=SL12345-1,password=NASPASSWORD 0 0
     ```
     {:pre}

   - If you don't want the storage to be mounted on restart, then go to the next step.

4. Verify that the `fstab` was edited correctly by unmounting and mounting the storage.
