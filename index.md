---
copyright:
  years: 1994, 2018
lastupdated: "2018-05-21"
---
{:shortdesc: .shortdesc}
{:note: .deprecated}
{:new_window: target="_blank"}

# Getting Started with NAS

NAS stands for network-attached storage. NAS is our earlier storage option for users who were looking for a solution similar to our LockBox storage but with more space. NAS allows for remote file storage directly from the server by using either command line/terminal interactions or through point-and-click interactions, if available. In addition to direct interaction with NAS from your server, you can also use Plesk or cPanel with File Transfer Protocol (FTP) to transfer files to NAS. FTP is complimentary with any NAS service, and NAS was offered at a nominal monthly fee based on the amount of storage.

IBM Cloud ended the sales (EOS) of NAS FTP storage services across all sales channels on **March 31, 2018**.

How does the EOS impact you?

- New customers aren't able to buy NAS FTP storage after **March 31, 2018**.
- Existing customers are able to use already provisioned NAS FTP storage after **March 31, 2018**, but aren't able to provision additional NAS FTP storage.

We recommend that you explore our [IBM Cloud storage solutions](https://www.ibm.com/cloud/storage) such as Block or File storage. They have both tiered and custom performance options up to 48,000 IOPS and capacity up to 12 TB. No matter your workloads, we have an easily customizable and cost-effective storage environment for you.

For more information or questions, please contact sales or support.<br />
(https://www.ibm.com/cloud-computing/bluemix/contact-us)


## Viewing storage information

Storage details regarding your File Storage (NAS) service can be viewed by using the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} at any time. You can view details such as password, storage address, and usage.

1. Access the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} using your unique credentials.
2. Select **Storage > File Storage** from the navigation bar to access the NAS screen.
2. Click anywhere on the row of the NAS to view its storage details.
3. Click the **Show** check box next to the **Password**  field to view the password for the selected NAS service.

## Changing the password for a NAS storage service

Each NAS storage service has an associated password that is used to access the NAS service in the command line of your operating system.  
For many of our {{site.data.keyword.BluSoftlayer_full}} products and services, the password storage feature within the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} is used solely for storage or tracking of the password and changes made to the password within the {{site.data.keyword.slportal}} aren't applied to the product or service. This is not the case for the NAS service.

Changes made to the NAS password within the {{site.data.keyword.slportal}} will be made to the service itself. Please make changes while keeping in mind that they will impact your service directly.

Follow the steps below to change a NAS password in the {{site.data.keyword.slportal}}.

1. Access the NAS Storage screen on the [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}.
2. Click anywhere on the row for the NAS storage to expand the view.
3. Click the **Show** check box to view your current password.
4. Enter the new password in the **Password** field.
5. Click the **Update** button.
