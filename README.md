![image](https://github.com/user-attachments/assets/feee8834-9801-464f-9df5-33025fc6e6d0)


# **Setting Up a Virtual Machine in Azure and Testing VPN Connection**

This tutorial will walk you through the process of setting up a Virtual Machine (VM) in Azure, configuring a VPN connection using ProtonVPN, and then cleaning up the resources. By the end of this tutorial, you will have successfully tested browsing behavior based on different geographic locations and VPN server locations.

## **Prerequisites**
Before starting, make sure you have:
- An Azure account (Sign up at [Azure](https://azure.microsoft.com/)).
- A ProtonVPN account (Sign up for the free version at [ProtonVPN](https://account.protonvpn.com/signup?plan=free&language=en)).
  ![image](https://github.com/user-attachments/assets/f97911e6-3edb-4f4c-8e3d-23ba694899f2)
  ![image](https://github.com/user-attachments/assets/c261bfd4-1099-4fd7-b82d-a2987c409767)





---

## **Step 1: Create a Virtual Machine in Azure**

### 1.1 Browse to WhatIsMyIP on Your Local Machine
1. Open your web browser on your local machine (the one you are physically using) and go to [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Take note of the public IP address displayed on the page. Copy it and save it to a text file for later comparison. This is my IPv4 address 
![image](https://github.com/user-attachments/assets/186a00ca-8bcd-4aec-944a-c86be352b3a3)




### 1.2 Create a Resource Group
1. Sign in to the [Azure Portal](https://portal.azure.com/).
2. In the left-hand menu, click on **Resource Groups**.
3. Click **+ Create** to create a new resource group.
4. Enter a name for the resource group (e.g., `MyResourceGroup`) and choose a region that is closest to your physical location.
5. Click **Review + Create**, then click **Create** to finalize the resource group creation.
    ![image](https://github.com/user-attachments/assets/e64c7ad1-fda9-411b-a097-6362ee1ee399)


### 1.3 Create a Windows 10 Virtual Machine (VM) in Another Geographic Location
1. In the Azure portal, go to **Virtual Machines** in the left-hand menu.
2. Click **+ Create** and then select **Windows 10** from the list of available images.
3. Choose a different geographic location for the VM (e.g., United Kingdom, Canada, or any other country outside your current location).
4. Configure the virtual machine:
   - Choose an appropriate **VM size**.
   - Create a **username** and **password** for the VM.
   - Under **Public IP**, ensure it's set to **Static**.
5. Click **Review + Create**, then click **Create** to deploy the VM.
      ![image](https://github.com/user-attachments/assets/f32166d0-0d25-45a7-80c9-864ec8f88983)
  ![image](https://github.com/user-attachments/assets/ce69d9e9-c0e1-48fa-815c-c6b930f690d7)

### 1.4 Log into the Virtual Machine Using Remote Desktop (RDP)
1. Once the VM is deployed, go to the **Overview** tab of the VM.
2. Click on the **Connect** button and choose **RDP** to download the RDP file.
3. Open the downloaded RDP file, then enter the **username** and **password** you set during the VM creation process to log in.

### 1.5 Browse to WhatIsMyIP on the VM
1. Once logged into the VM, open a web browser inside the VM and go to [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Note the public IP address displayed here. Copy it and save it in the same text file used earlier for comparison.
   ![image](https://github.com/user-attachments/assets/68e30a44-27e3-44c6-b741-6ea294361d10)


---

## **Step 2: Sign Up for ProtonVPN and Test the VPN Connection**

### 2.1 Sign Up for ProtonVPN (On Your Local Machine)
1. Visit [ProtonVPN Signup](https://account.protonvpn.com/signup?plan=free&language=en) on your local machine.
2. Follow the instructions to sign up for a free ProtonVPN account.
3. Once signed up, note your credentials (username and password) for logging in.
   ![image](https://github.com/user-attachments/assets/c20e3164-1c59-4a08-acba-845b87f3ad9f)


### 2.2 Download and Install ProtonVPN on the Virtual Machine
1. On your VM, open a web browser and visit [ProtonVPN Downloads](https://protonvpn.com/download).
2. Download and install the ProtonVPN client for **Windows**.
3. After installation, launch ProtonVPN on the VM.
   ![image](https://github.com/user-attachments/assets/1020a32f-7f04-419b-81c0-dce34c497f71)
   ![image](https://github.com/user-attachments/assets/3b5a5620-e7bd-4973-915b-e41c618db0a1)
   ![image](https://github.com/user-attachments/assets/40330f62-a2b9-4506-93f3-a0001f723718)
   ![image](https://github.com/user-attachments/assets/234abc37-4d7c-4e1b-8c49-a9c671b8339c)
   ![image](https://github.com/user-attachments/assets/1cec4150-e1c1-4acc-8e3b-2f78a01864f7)

  

 







### 2.3 Log In and Connect to a VPN Server in a Different Country
1. Open ProtonVPN and log in with the credentials you created in Step 2.1.
2. Choose a VPN server located in a different country, such as Japan.
3. Click **Connect** to establish the VPN connection.
   ![image](https://github.com/user-attachments/assets/a021956b-a13c-4e1a-831a-de5c43cd8fc6)
   ![image](https://github.com/user-attachments/assets/1408006c-21b1-4337-8e68-03e55d0ad777)
   ![image](https://github.com/user-attachments/assets/7a2416bc-01cc-4057-ac2b-612aa3fb1ccb)
   ![image](https://github.com/user-attachments/assets/9221ef2a-fb03-4311-9954-bfcfd87b8c0f)
   ![image](https://github.com/user-attachments/assets/e72846e7-b954-4e55-9907-35810c18e351)

  



### 2.4 Browse to WhatIsMyIP on the VM (While Connected to the VPN)
1. With ProtonVPN connected, open a web browser in the VM and visit [https://whatismyipaddress.com/](https://whatismyipaddress.com/).
2. Take note of the new public IP address, which should reflect the location of the VPN server you connected to (e.g., Japan).
3. Save this IP address in the same text file for later comparison.
   <h2> Previous VM'S: IPv4 Address</h2>

    ![image](https://github.com/user-attachments/assets/68e30a44-27e3-44c6-b741-6ea294361d10)  


   <h2> New VM'S: IPv4 Address after using VPN</h2>

   ![image](https://github.com/user-attachments/assets/fc6e2324-e1e0-4cdc-92f5-9c45caeb8841)

   <h2> Connected to New VPN location within VM</H2>
   
   ![image](https://github.com/user-attachments/assets/4abfd483-1589-49f2-8c2e-ee863f793a76)


### 2.5 Test Browsing Behavior with the VPN
1. Try visiting websites like [Google](https://www.google.com/), [Disney](https://www.disney.com/), or [Amazon](https://www.amazon.com/) while connected to the VPN.
2. Note any differences you observe in the website’s language, layout, or URL based on the location of the VPN server. For example:
   - You may be redirected to a **localized version** of Google (e.g., google.jp if you’re connected to a Japanese server).
   - The language of the website may automatically change to the country’s native language (e.g., Japanese, French, etc.).
     ![image](https://github.com/user-attachments/assets/00cada41-991f-42d6-a2d7-8dd6d48258cf)
     ![image](https://github.com/user-attachments/assets/0c05a541-0106-4ba9-b545-f121494c8b62)
     ![image](https://github.com/user-attachments/assets/d6c5dbb8-b82f-4323-9345-7dd23df9467c)




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





