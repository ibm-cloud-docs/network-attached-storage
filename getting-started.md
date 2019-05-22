---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

keywords:

subcollection: network-attached-storage

---
{:deprecated: .deprecated}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}
{:external: target="_blank" .external}

# Getting started tutorial
{: #GettingStarted}

NAS stands for network-attached storage. NAS was an earlier storage option for users who were looking for a solution similar to the LockBox storage but with more space. IBM Cloud ended the sales (EOS) of NAS FTP storage services across all sales channels on **31 March 31 2018**. End of Support commenced on **16 August 16 2018**.

All instances of this service are deprecated. For more information, contact [sales or support](https://www.ibm.com/cloud-computing/bluemix/contact-us).
{:deprecated}

Customers can no longer provision this storage and are urged to migrate their data to another Storage offering such as Block or File storage. For more information, see the [IBM Cloud storage solutions](https://www.ibm.com/cloud/storage). They have both tiered and custom performance options up to 48,000 IOPS and capacity up to 12 TB. No matter your workloads, {{site.data.keyword.BluSoftlayer_full}} has an easily customizable and cost-effective storage environment for you.

## Using alternatives for NAS FTP storage

* {{site.data.keyword.filestorage_full}}
  - [Configuring {{site.data.keyword.filestorage_short}} for backup with cPanel](/docs/infrastructure/FileStorage/migrate-file-storage-encrypted-file-storage.htm?topic=FileStorage-cPanelBackups)
  - [Configuring {{site.data.keyword.filestorage_short}} for backup with Plesk](/docs/infrastructure/FileStorage/migrate-file-storage-encrypted-file-storage.htm?topic=FileStorage-PleskBackup)

* {{site.data.keyword.blockstoragefull}}
  - [Configuring {{site.data.keyword.blockstorageshort}} for backup with cPanel](/docs/infrastructure/BlockStorage?topic=BlockStorage-cPanelBackups)
  - [Configuring {{site.data.keyword.blockstorageshort}} for backup with Plesk](/docs/infrastructure/BlockStorage?topic=BlockStorage-PleskBackups)

* {{site.data.keyword.cos_full}}
  - [Mounting {{site.data.keyword.cos_short}} with s3fuse](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-MountCOSs3fuse)


## Viewing NAS FTP storage Information

Storage details of your File Storage (NAS) service can be viewed in the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} at any time. You can view details such as password, storage address, and usage.

1. Log in to the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} with your unique credentials.
2. Select **Storage > File Storage** from the navigation bar to access the NAS screen.
2. Click anywhere on the row of the NAS to view its storage details.

## Changing the password for a NAS storage service

Each NAS storage service has a password that is used to access the NAS service in the command line or prompt of your operating system.

For many of the {{site.data.keyword.BluSoftlayer_full}} products and services, the password storage feature within the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} is used solely for storage or tracking of the password. However, the changes that are made to the NAS password within the {{site.data.keyword.slportal}} are also made to the service itself. When you change your password, keep in mind that the change impacts your service directly.

Follow these steps to change a NAS password in the {{site.data.keyword.slportal}}.

1. Access the NAS Storage screen on the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}.
2. Click anywhere on the row for the NAS storage to expand the view.
3. Click **Show** next to the **Password** field to view your current password.
4. Enter the new password in the **Password** field.
5. Click **Update**.

## Frequently asked questions

**Can NAS be used to store files from personal devices?**

{{site.data.keyword.BluSoftlayer_full}} allows files from devices on the {{site.data.keyword.BluSoftlayer_full}} network to be stored with NAS. Files on personal devices are not eligible for NAS. However, any file from a device on the {{site.data.keyword.BluSoftlayer_full}} network can be stored with NAS.

**Why can't the {{site.data.keyword.slportal}} be used to connect devices and store files on NAS?**

Mounting or connecting NAS and configuring FTP connections varies based on the operating system or control panel you are using. Within each individual system or panel, configuration options are unique. Some systems offer a robust set of options to customize your remote storage, while some systems allow for more basic configurations. Therefore, working directly in your system provides the best result from a client perspective.
