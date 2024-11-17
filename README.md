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

### 1.4 Log into the Virtual Machine Using Remote Desktop (RDP)
1. Once the VM is deployed, go to the **Overview** tab of the VM.
2. Click on the **Connect** button and choose **RDP** to download the RDP file.
3. Open the downloaded RDP file, then enter the **username** and **password** you set during the VM creation process to log in.

### 1.5 Browse to WhatIsMyIP on the VM
1. Once logged into the VM, open a web browser inside the VM and go to [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Note the public IP address displayed here. Copy it and save it in the same text file used earlier for comparison.

---

## **Step 2: Sign Up for ProtonVPN and Test the VPN Connection**

### 2.1 Sign Up for ProtonVPN (On Your Local Machine)
1. Visit [ProtonVPN Signup](https://account.protonvpn.com/signup?plan=free&language=en) on your local machine.
2. Follow the instructions to sign up for a free ProtonVPN account.
3. Once signed up, note your credentials (username and password) for logging in.

### 2.2 Download and Install ProtonVPN on the Virtual Machine
1. On your VM, open a web browser and visit [ProtonVPN Downloads](https://protonvpn.com/download).
2. Download and install the ProtonVPN client for **Windows**.
3. After installation, launch ProtonVPN on the VM.

### 2.3 Log In and Connect to a VPN Server in a Different Country
1. Open ProtonVPN and log in with the credentials you created in Step 2.1.
2. Choose a VPN server located in a different country, such as Japan.
3. Click **Connect** to establish the VPN connection.

### 2.4 Browse to WhatIsMyIP on the VM (While Connected to the VPN)
1. With ProtonVPN connected, open a web browser in the VM and visit [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Take note of the new public IP address, which should reflect the location of the VPN server you connected to (e.g., Japan).
3. Save this IP address in the same text file for later comparison.

### 2.5 Test Browsing Behavior with the VPN
1. Try visiting websites like [Google](https://www.google.com/), [Disney](https://www.disney.com/), or [Amazon](https://www.amazon.com/) while connected to the VPN.
2. Note any differences you observe in the website’s language, layout, or URL based on the location of the VPN server. For example:
   - You may be redirected to a **localized version** of Google (e.g., google.jp if you’re connected to a Japanese server).
   - The language of the website may automatically change to the country’s native language (e.g., Japanese, French, etc.).

---

## **Step 3: Clean Up Azure Resources**

### 3.1 Delete the Resource Group
1. Go back to the **Azure Portal** and navigate to **Resource Groups**.
2. Select the resource group you created earlier (e.g., `MyResourceGroup`).
3. Click on the **Delete** button.
4. Confirm the deletion by typing the name of the resource group and clicking **Delete**.

### 3.2 Verify Deletion of Resources
1. Once the resource group has been deleted, make sure all resources, including the VM and associated components (e.g., networking resources), have been removed from your Azure subscription.
2. This will prevent any further charges for resources that are no longer in use.

---

## **Conclusion**
In this tutorial, you have:
- Created a Windows 10 VM in Azure located in a different geographic region.
- Used ProtonVPN to connect to a server in another country and tested website behavior based on your VPN location.
- Cleaned up your Azure resources to avoid ongoing charges.

By following these steps, you now have a practical understanding of managing resources in Azure and using a VPN for testing geographical variations in browsing behavior.

---

Feel free to **fork** this repository and add your own experiences or improvements!



