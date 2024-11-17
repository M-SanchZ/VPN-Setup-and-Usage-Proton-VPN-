![image](https://github.com/user-attachments/assets/8653a0cb-e838-4d5d-88a4-5a23e613dbf6)

# **Setting Up a Virtual Machine in Azure and Testing VPN Connection**

This tutorial will walk you through the process of setting up a Virtual Machine (VM) in Azure, configuring a VPN connection using ProtonVPN, and then cleaning up the resources. By the end of this tutorial, you will have successfully tested browsing behavior based on different geographic locations and VPN server locations.

## **Prerequisites**
Before starting, make sure you have:
- An Azure account (Sign up at [Azure](https://azure.microsoft.com/)).
- A ProtonVPN account (Sign up for the free version at [ProtonVPN](https://account.protonvpn.com/signup?plan=free&language=en)).

---

## **Step 1: Create a Virtual Machine in Azure**

### 1.1 Browse to WhatIsMyIP on Your Local Machine
1. Open your web browser on your local machine (the one you are physically using) and go to [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Take note of the public IP address displayed on the page. Copy it and save it to a text file for later comparison.

### 1.2 Create a Resource Group
1. Sign in to the [Azure Portal](https://portal.azure.com/).
2. In the left-hand menu, click on **Resource Groups**.
3. Click **+ Create** to create a new resource group.
4. Enter a name for the resource group (e.g., `MyResourceGroup`) and choose a region that is closest to your physical location.
5. Click **Review + Create**, then click **Create** to finalize the resource group creation.

### 1.3 Create a Windows 10 Virtual Machine (VM) in Another Geographic Location
1. In the Azure portal, go to **Virtual Machines** in the left-hand menu.
2. Click **+ Create** and then select **Windows 10** from the list of available images.
3. Choose a different geographic location for the VM (e.g., United Kingdom, Canada, or any other country outside your current location).
4. Configure the virtual machine:
   - Choose an appropriate **VM size**.
   - Create a **username** and **password** for the VM.
   - Under **Public IP**, ensure it's set to **Static**.
5. Click **Review + Create**, then click **Create** to deploy the VM.

### 1.4 Log into the Virtual Ma



