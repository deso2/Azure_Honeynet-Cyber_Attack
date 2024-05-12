# Azure_Honeynet-Cyber_Attack

<img width="700" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/8f051c79-7cd9-47a4-a0c9-e0b3466e58ab">

This is a continuation of setting up the <a href="https://github.com/deso2/VM-HoneyPot-Configuration/blob/main/README.md">Virtual Machine</a> for a honeypot environment. After setting up the VM on Azure, check the status if it connected. I Used a windows vm to connect remotely using RDP.

<img width="701" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/aa8b841d-afbf-46e6-aab8-d1a3e56962e0">

<img width="618" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/432d33e8-148f-4582-b6a1-562b36ddd850">

Signed up for an account to [](https://ipgeolocation.io/) and receive a IP API that provides country, city, state, province, local currency, latitude and longitude and insert it into a custom script.

<img width="509" src="https://github.com/deso2/Azure_Honeynet-Cyber_Attack/assets/168561314/f49f010f-bd30-4706-b11f-19889f98ba77">

Once connected, open PowerShell and use a custom script. This script will configure the latitude and longitude in the logs, extracting all events with login failures and creating a new log file using an IP geolocation API.

At the top of the script, make sure to modify the $API_key variable with your API key. After updating the script, execute it and allow it to run its course.

Next, we'll create a spot for log analytics on Azure. This will involve providing sample log events to train the system on what to look for in the Log Analytics workspace. Navigate to the table toolbar on the left, click on the '+' icon, and select 'Create New Custom Log (MMA-based)'. Choose the failed_rdp log file as the sample log, and give the custom log a name of your choice.

Finally, you can proceed with any additional manual steps
