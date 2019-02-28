---

copyright:
  years: 1994, 2019
lastupdated: "2019-02-05"

keywords: NAS, cPanel, Backups, WHM

subcollection: network-attached-storage

---
{:deprecated: .deprecated}
{:DomainName: data-hd-keyref="APPDomain"}
{:DomainName: data-hd-keyref="DomainName"}
{:new_window: target="_blank"}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}

# Configuring FTP for NAS with cPanel and WHM
{: #configureNAScPanel}

All instances of this service are deprecated. For more information, contact [support](https://www.ibm.com/cloud-computing/bluemix/contact-us).
{:deprecated}

You can use NAS with cPanel and WHM for your backups. You can load data through File Transfer Protocol (FTP) to your NAS storage device. Follow these steps to configure FTP for your NAS within cPanel and WHM.

1. Log in to WHM with your unique credentials.

2. On the **Home** screen, select **Configure backup** from the **backup** menu.

3. Update the **Configuration Options** based on your backup preferences.

   <table>
   <tr>
     <th>Configuration option</th>
     <th>Entry</th>
   </tr>
   <tr>
     <td>`Backup type`</td>
     <td>Remote FTP (Accounts Only)</td>
   </tr>
   <tr>
     <td>`Remote FTP Host`</td>
     <td>The host name for the NAS storage</td>
   </tr>
   <tr>
     <td>`FTP backup User`</td>
     <td>The host name for the NAS storage</td>
   </tr>
   <tr>
     <td>`FTP backup pPassword`</td>
     <td>The password that is associated with the selected NAS.</td>
   </tr>
   </table>

   For more information about configuration options, see [cPanel's wiki ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://docs.cpanel.net/display/68Docs/Backup+Configuration#70704c1ed4aa4817b989519beca3f78d){:new_window}.

4. Click the **Save** button to save the configuration.

5. Run the following script to test the configuration:

   ```
   /usr/local/cpanel/scripts/cpbackup
   ```
   {: pre}

   If the configuration was not updated correctly, repeat the same steps.
   {:tip}
