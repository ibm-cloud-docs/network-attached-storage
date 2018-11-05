---
copyright:
  years: 1994, 2018
lastupdated: "2018-08-16"
---
{:pre: .pre}
{:deprecated: .deprecated}
{:new_window: target="_blank"}

# Connecting to NAS Storage in Windows

**This service is deprecated**: All instances of this service are deprecated. For more information, contact [sales or support](https://www.ibm.com/cloud-computing/bluemix/contact-us).
{:deprecated}

You can map NAS storage in Windows either in the command line or through point-and-click interaction in the File Explorer.

## Mapping the Storage through the command prompt

If you want to map to LockBox through the command prompt, enter the following command.
   ```
   net use {drive letter}: \\Hostname\Username /u:username password
   ```
   {: pre}
   
   Example
   ```
   net use z: \\nas0X.service.softlayer.com\auser /u:auser apass
   ```

## Mapping the Storage through Explorer

1. Open File Explorer.
2. Select **Map network drive**.
3. Select the **Drive Letter** that you want from the **Drive** list.
4. Enter the path to the LockBox in the **Folder** field. <br/>
   `\\nas0X.service.softlayer.com\{NASusername}`
5. Select the **Connect using different credentials** option.
6. You can select the **Reconnect at logon** check box to automatically reconnect to the LockBox.
7. Click the **Finish** to complete the mapping process. When you are prompted for credentials,
  * Enter the NAS user name in the **User name** field.
  * Enter the NAS password in the **Password** field.
  * Click **OK**
