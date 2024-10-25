# Active Directory & User Management with PowerShell (Homelab) Walkthrough

  <img src="https://github.com/user-attachments/assets/f594a2ef-64b6-483c-8476-8585356d4226" height="80%" width="80%" alt=""/>

## Description
This project involves setting up a home lab using Oracle VirtualBox to create a network environment with Windows 10 and Windows Server 2019. The lab will utilize Active Directory (AD) for user management, leveraging PowerShell to automate the creation of random users. This setup aims to provide hands-on experience in managing AD, enhancing skills in Windows Server administration, and scripting with PowerShell. Users will learn how to configure AD, implement user policies, and generate user accounts efficiently through PowerShell commands.

## Languages and Utilities Used

- **PowerShell**

## Environments Used 

- **Windows 10**
- **Windows Server 2019**
- **Oracle VirtualBox**

## Step-by-Step Instructions

### Step 1: Set Up Your Environment
Start by installing Oracle VirtualBox on your host machine. This software will allow you to create and manage virtual machines.

<img src="https://github.com/user-attachments/assets/6d323fd1-f7b9-4a89-bbbf-5996e991a275" height="80%" width="80%" alt=""/>

### Step 2: Install Windows Server
1. Open VirtualBox and create a new VM:
   - Click on **New** and select **Windows Server 2019** as the version.
   - Allocate memory and disk space as per your requirements.
2. Mount the Windows Server ISO you obtained earlier.
3. Start the VM and follow the installation prompts to install Windows Server.

<img src="https://github.com/user-attachments/assets/ccaa7320-565a-4430-91f2-beea963965cf" height="80%" width="80%" alt=""/>

<img src="https://github.com/user-attachments/assets/a5af0a16-2904-44d0-865a-fcd40b87542b" height="80%" width="80%" alt=""/>

### Step 3: Install Guest Additions and Configure Static IP Address
1. Once the Windows Server installation is complete, install the Guest Additions to improve performance:
   - Go to the VirtualBox menu and select **Devices > Insert Guest Additions CD Image**.
2. Change the server's hostname:
   - Go to **Server Manager > Local Server** and find the **Computer Name** section. Click on **Change**.
3. Set a static IP address on the internal network:
   - Navigate to **Network and Sharing Center**, select **Change adapter settings**, right-click on the network adapter, and select **Properties**. Configure the IP address.

<img src="https://github.com/user-attachments/assets/05883df9-5837-4f17-aeb6-ed4c4727e7b4" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/aff86e5e-177b-4243-b7ee-0f77de9da5f7" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/a2c06ceb-8165-4949-8b24-7f0380f6d31e" height="80%" width="80%" alt=""/>

### Step 4: Configure Server Roles
1. Open **Server Manager**. You will see a dashboard with server information.
2. Click on **Add roles and features** to open the wizard.
3. Select **Role-based or feature-based installation** and choose your server from the server pool.
4. Install the following roles:
   - **DHCP Server**
   - **Routing**

<img src="https://github.com/user-attachments/assets/fc43bf13-15fc-4b70-a83c-75b3bb38e283" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/02e9444b-0a02-4452-9f6d-ed549f53f75d" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/9f5cdd40-b2ed-4ea8-9917-39011c35f1dc" height="80%" width="80%" alt=""/>


### Step 5: Promote to Domain Controller
1. In Server Manager, you will see a notification flag indicating the AD DS role has been installed. Click on it to promote the server to a Domain Controller.
2. Use the **Active Directory Domain Services Configuration Wizard**:
   - Choose to add a new forest and enter **mydomain.com** as the domain name.
3. Complete the wizard and allow the server to restart.

<img src="https://github.com/user-attachments/assets/762ddc78-9ea0-42db-a143-3610bc408ed7" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/6453f479-883f-49e3-82cd-12748d03e7ac" height="80%" width="80%" alt=""/>

### Step 6: Configure Routing and Remote Access

After promoting your server, access **Routing and Remote Access** from Server Manager.

1. Click on **Configure and Enable Routing and Remote Access**.
2. Proceed with the default options by clicking **Next**.
3. Choose **NAT** for the network topology and select the **Internal Network** option.
   
<img src="https://github.com/user-attachments/assets/eb2de298-86a3-4e58-bdfa-3874a32c1ed6" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/9d14f2a8-b537-4e24-bc85-bed49b38fc0c" height="80%" width="80%" alt=""/>

### Step 7: Manage Active Directory
1. Open **Active Directory Users and Computers** from the Administrative Tools menu.
2. Create a new IP address scope for the DHCP server and configure it as needed.
3. Add users to **mydomain.com** by right-clicking on the Users container and selecting **New > User**.

<img src="https://github.com/user-attachments/assets/5f4dac4a-3e1e-4e90-8ce4-682636a46cc6" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/a418474c-e6ff-4c77-8e61-1fa6463cb9c6" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/18b22b8f-21e7-4dd4-9c76-9c78b04dbf73" height="80%" width="80%" alt=""/>

### Step 8: Test Windows Client Connectivity
1. Open your Windows 10 client VM and check if it’s connected to the **mydomain.com** server.
2. Rename the PC:
   - Go to **System Properties**, click on **Change settings**, and rename it to **Client 1**.
3. Join the domain by entering **mydomain.com** and providing domain credentials.
4. Log in using the user accounts created on the server.

<img src="https://github.com/user-attachments/assets/2730a84b-13ed-4425-98eb-6c3c522fb3bc" height="80%" width="80%" alt=""/>
<img src="https://github.com/user-attachments/assets/0a01696b-39d1-48fe-98ed-2177a16b842d" height="80%" width="80%" alt=""/>

### Step 9: Automate User Creation with PowerShell
1. Open PowerShell as an administrator on your server.
2. Use the provided PowerShell script to create random users:
   - Download the script from this repository.
   - Run the script to create users automatically in Active Directory.

   **Screenshot**: (Include a screenshot of the PowerShell script in action.)

## Conclusion
Congratulations! You've successfully set up an Active Directory environment and learned how to manage user accounts using PowerShell. This configuration is essential for any network administrator and will enhance your skills in Windows server management.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
Thanks for following along! If you have any questions or feedback, feel free to reach out.


