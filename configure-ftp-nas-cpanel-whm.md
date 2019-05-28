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
{:external: target="_blank" .external}
{:external: target="_blank" .external}
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

| Configuration option | Entry |
|-----|-----|
| `Backup type` | Remote FTP (Accounts Only) |
| `Remote FTP Host` | The host name for the NAS storage |
| `FTP backup User` | The user name for the NAS storage< |
| `FTP backup pPassword` | The password that is associated with the selected NAS |
{: caption="Table 1. Configuration options" caption-side="top"}

   For more information about configuration options, see [cPanel's wiki](https://docs.cpanel.net/display/68Docs/Backup+Configuration#70704c1ed4aa4817b989519beca3f78d){: external}.

4. Click the **Save** button to save the configuration.

5. Run the following script to test the configuration:

   ```
   /usr/local/cpanel/scripts/cpbackup
   ```
   {: pre}

   If the configuration was not updated correctly, repeat the same steps.
   {:tip}
