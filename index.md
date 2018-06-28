---
copyright:
  years: 1994, 2018
lastupdated: "2018-06-28"
---
{:note: .deprecated}
{:new_window: target="_blank"}

# Getting Started with NAS

NAS stands for network-attached storage. NAS was an earlier storage option for users who were looking for a solution similar to the LockBox storage but with more space. NAS allows for remote file storage directly from the server by using either command line/terminal interactions or through point-and-click interactions. In addition to direct interaction with NAS from your server, you can also use Plesk or cPanel with File Transfer Protocol (FTP) to transfer files to NAS. FTP is complimentary with any NAS service, and NAS was offered at a nominal monthly fee based on the amount of storage.

IBM Cloud ended the sales (EOS) of NAS FTP storage services across all sales channels on **March 31, 2018**.

How does the EOS impact you?

- New customers can't buy NAS FTP storage after **March 31, 2018**.
- Existing customers can continue to use their NAS FTP storage after **March 31, 2018**, but can't provision more NAS FTP storage.

Explore the [IBM Cloud storage solutions](https://www.ibm.com/cloud/storage) such as Block or File storage. They have both tiered and custom performance options up to 48,000 IOPS and capacity up to 12 TB. No matter your workloads, {{site.data.keyword.BluSoftlayer_full}} has an easily customizable and cost-effective storage environment for you.

For more information or questions, contact sales or support.<br />
(https://www.ibm.com/cloud-computing/bluemix/contact-us)


## Viewing storage Information

Storage details of your File Storage (NAS) service can be viewed in the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} at any time. You can view details such as password, storage address, and usage.

1. Log in to the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} with your unique credentials.
2. Select **Storage > File Storage** from the navigation bar to access the NAS screen.
2. Click anywhere on the row of the NAS to view its storage details.

## Changing the password for a NAS storage service

Each NAS storage service has a password that is used to access the NAS service in the command line/prompt of your operating system.

For many of the {{site.data.keyword.BluSoftlayer_full}} products and services, the password storage feature within the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} is used solely for storage or tracking of the password. However, the changes that are made to the NAS password within the {{site.data.keyword.slportal}} are also made to the service itself. When you change your password, keep in mind that the change impacts your service directly.

Follow these steps to change a NAS password in the {{site.data.keyword.slportal}}.

1. Access the NAS Storage screen on the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}.
2. Click anywhere on the row for the NAS storage to expand the view.
3. Click **Show** next to the **Password** field to view your current password.
4. Enter the new password in the **Password** field.
5. Click **Update**.

## Frequently asked questions

**Can NAS be used to store files from personal devices?**

{{site.data.keyword.BluSoftlayer_full}} allows files from devices on the {{site.data.keyword.BluSoftlayer_full}} network to be stored with NAS. Files on personal devices are not eligible for NAS. However, any file from a device on the {{site.data.keyword.BluSoftlayer_full}} network can be stored with NAS.

**Why can't the {{site.data.keyword.slportal}} be used to connect devices and store files on NAS?**

Mounting or connecting NAS and configuring FTP connections varies based on the operating system or control panel you are using. Within each individual system or panel, configuration options are unique. Some systems offer a robust set of options to customize your remote storage, while some systems allow for more basic configurations. Therefore, working directly in your system provides the best result from a client perspective.
