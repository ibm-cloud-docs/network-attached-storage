---
copyright:
  years: 1994, 2018
lastupdated: "2018-06-28"
---
{:pre: .pre}
{:note: .deprecated}
{:new_window: target="_blank"}

# Configuring FTP for NAS with cPanel and WHM

You can use NAS with cPanel and WHM for your backups. You can load data through File Transfer Protocol (FTP) to your NAS storage device. Follow these steps to configure FTP for your NAS within cPanel and WHM.

## Configuring FTP

1. Log in to WHM with your unique credentials.

2. On the **Home** screen, select **Configure Backup** from the **Backup** menu.

3. Update the **Configuration Options** based on your backup preferences.

   | Configuration Option | Entry |
   | --- | --- |
   | Backup Type | Remote FTP (Accounts Only) |
   | Remote FTP Host | The host name for the NAS storage |
   | FTP Backup User | The user name that is associated with the selected NAS |
   | FTP Backup Password |The password that is associated with the selected NAS |
   
   For more information about configuration options, see [cPanel's wiki](https://docs.cpanel.net/display/68Docs/Backup+Configuration#70704c1ed4aa4817b989519beca3f78d){:new_window}.

4. Click the **Save** button to save the configuration.

5. Run the following script to test the configuration:

   ```
   /usr/local/cpanel/scripts/cpbackup
   ```
   {: pre}
   
   **Note** - If the configuration was not updated correctly, repeat the same steps.
