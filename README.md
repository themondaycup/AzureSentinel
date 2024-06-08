<h1>Microsoft Azure Sentinel | Using a SIEM for live attacks</h1>

Huge thanks to Josh Madakor for creating this awesome lab! It was really fun to recreate and learn about. His video can be found [here](https://youtu.be/RoZeVbbZ0o0?si=2d2N-lM7PYsF8Twc)

<h2>Learning Objectives:</h2>

- Configuration & Deployment of Microsoft Azure virtual machines, Log Analytics Workspaces, and Microsoft Sentinel
- Hands-on experience with Microsoft Sentinel, a cloud-native SIEM (Security Information and Event Management)
- Understanding Windows Security Event logs
- Using Kusto Query Language (KQL) to query logs
- Displaying attack data on a dashboard with Workbooks (Viewing it as a World Map)

<h2>Tools</h2>

- Microsoft Azure
- Remote Desktop Protocol
- 3rd party API:  [IP Geolocation](https://ipgeolocation.io/)
- Custom [powershell script](https://github.com/joshmadakor1/Sentinel-Lab/blob/main/Custom_Security_Log_Exporter.ps1) by Josh Madakor

### Overview
![](images/setting%20up%20sentinel%20(SIEM).jpg)

<h2>Steps</h2>
  
### Creating a Microsoft Azure account
> Creating a new Azure account to have $200 credit for 30 days

![](images/Azure.jpg)

### Creating a Virtual Machine to be our Honeypot
> I went back to change the machine size so it was not running slowly

![](images/creating%20VM.jpg)

### Changing VM security to allow all inbound traffic
> Only did this so the machine can be found faster

![](images/allow%20all%20in%20firewall.jpg)

### Log Analytics Workspace
>Purpose of this is to ingest logs from the VM, create a log with the data, then have it be seen in the SIEM

![](images/log%20analytics%20workspace.jpg)

### Changing Microsoft Defender for Cloud security

![](images/enable%20VM%20logs%20in%20MS%20Defender%20for%20Cloud.jpg)

![](images/enable%20VM%20logs%20in%20MS%20Defender%20for%20Cloud%202.jpg)

### Setting up Microsoft Sentinel
> Created the SIEM and then choose workbooks to add the honeypot

![](images/activing%20sentinel%20(SIEM).jpg)

### Log into VM with Remote Desktop
> Once logged into VM I turned off Windows Firewall and tested the connection

![](images/RDP%20into%20VM.jpg)

![](images/testing%20to%20see%20if%20VM%20firewall%20is%20off.jpg)

### Using Custom powershell script and Making Free IP Geolocation account for API

![](images/powershell%20script.jpg)

### Waiting for logs to populate

![](images/Waiting%20for%20custom%20log%20to%20populate.jpg)

![](images/Waiting%20for%20custom%20log%20to%20populate%20-%20test%202.jpg)

### Map on inital set-up

![](images/Map1.jpg)

### End of Project
>left the VM running for roughly 4 hours before stopping it. This was my final results

![](images/map2.png)
