# Azure Honeynet Cyber Attack
<p align="center"><img width="700" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/8f051c79-7cd9-47a4-a0c9-e0b3466e58ab">

After setting up a <a href="https://github.com/deso2/VM-HoneyPot-Configuration/blob/main/README.md">Virtual Machine</a> for a honeypot environment, Check the status of your VM if it is online. Connect to it remotely, using the public IP on your Azure VM. I used RDP on my windows VM.

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/aa8b841d-afbf-46e6-aab8-d1a3e56962e0">

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/432d33e8-148f-4582-b6a1-562b36ddd850">

Signed up for an account to this [website](https://ipgeolocation.io/) and receive a IP API that provides country, city, state, province, local currency, latitude and longitude and insert it into a custom script.

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/f49f010f-bd30-4706-b11f-19889f98ba77">

Once connected, open PowerShell and paste a coustom script that will configure the latitude and longitude in the logs, extracting all events with login failures and creating a new log file using an IP geolocation API. At the top of the script, make sure to modify the $API_key variable with your API key. After updating the script, execute it and allow it to run its course.

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/46b69daa-7a31-41c0-8961-4d1dff6960dc">

Next, we'll create a spot for log analytics on Azure. This will involve providing sample log events to train the system on what to look for in the Log Analytics workspace. Navigate to the table toolbar on the left, click on the '+' icon, and select 'Create New Custom Log (MMA-based)'. 

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/0c36b042-936f-4254-bf3b-a030eb0869e3">

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/dbee01dd-0be5-40b3-b606-ec570ba1d63c">

Choose the failed_rdp log file as the sample log, and the path in ypur VM give the custom log a name of your choice.

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/2823e363-b7fd-41df-956d-6f8ce7f428dd">

<p align="center"><img width="670" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/13869ba0-92e3-46f4-8654-cc516ab111fc">

Run the query and use virtualization to map and adjust the settings according to your preferences. I adjusted mine to view attempts by country. Thank you for joining me in this walkthrough.
