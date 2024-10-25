# Active Directory & User Management with PowerShell (Homelab) Walkthrough

  <img src="https://github.com/user-attachments/assets/f594a2ef-64b6-483c-8476-8585356d4226" height="80%" width="80%" alt="Password Complexity Checker Code Overview"/>

## Description
This project involves setting up a home lab using Oracle VirtualBox to create a network environment with Windows 10 and Windows Server 2019. The lab will utilize Active Directory (AD) for user management, leveraging PowerShell to automate the creation of random users. This setup aims to provide hands-on experience in managing AD, enhancing skills in Windows Server administration, and scripting with PowerShell. Users will learn how to configure AD, implement user policies, and generate user accounts efficiently through PowerShell commands.

## Languages and Utilities Used

- **PowerShell**

## Environments Used 

- **Windows 10**
- **Windows Server 2019**
- **Oracle VirtualBox**

## Step-by-Step Instructions

### 1. Introduction
Active Directory (AD) is Microsoft’s directory service for Windows networks. It helps you manage users and resources centrally. A Domain Controller (DC) hosts AD and handles authentication requests.

### 2. Requirements
Before we dive in, make sure you have:
- **Oracle VirtualBox**
- **Windows 10 ISO**
- **Windows Server 2019 ISO**

  <img src="https://github.com/user-attachments/assets/73df22f2-7e24-455b-933f-cd51a69a0959" height="80%" width="80%" alt="Password Complexity Checker Code Overview"/>

### 3. Setting Up Oracle VirtualBox
1. **Download and install Oracle VirtualBox** from [the official site](https://www.virtualbox.org/).
2. **Create a new VM for Windows Server**:
   - Open VirtualBox and click "New" to start.
     
<img src="https://github.com/user-attachments/assets/947165b2-e80a-4bcd-8e48-0fd037a4b7c8" height="80%" width="80%" alt="Password Complexity Checker Code Overview"/>

### 4. Installing Windows Server
1. **Start your VM** and mount the Windows Server ISO.
2. **Follow the installation prompts**, selecting your language and version.

<img src="https://github.com/user-attachments/assets/9983f264-f5bf-45e4-bde2-3eb4fe916383" height="80%" width="80%" alt="Password Complexity Checker Code Overview"/>
<br />


<p align="center">
Code Overview: <br/>
<img src="https://github.com/user-attachments/assets/aa91d9b6-9557-4595-8157-7c14b7762f91" height="80%" width="80%" alt="Password Complexity Checker Code Overview"/>
<br />
<br />
Testing for Strong, Moderate, and Weak Passwords: <br/>
<img src="https://github.com/user-attachments/assets/42648c04-d60e-4581-81aa-3e92f036fb2a" height="80%" width="80%" alt="Testing Strong Password"/>
<br />
<img src="https://github.com/user-attachments/assets/78ff35f4-64a9-4264-a533-12c149069ee4" height="80%" width="80%" alt="Testing Moderate Password"/>
<br />
<img src="https://github.com/user-attachments/assets/fcd343f1-129f-43c0-a6d1-c5963206bce6" height="80%" width="80%" alt="Testing Weak Password"/>
</p>

## How It Works:
- **Length**: At least 8 characters.
- **Uppercase**: Includes one uppercase letter.
- **Lowercase**: Includes one lowercase letter.
- **Number**: Contains at least one digit.
- **Special Character**: Includes one special character (e.g., `!@#$%^&*()`).

## Usage
1. **Run the Script**: Input your password when prompted.
2. **View Feedback**: The script will return whether your password is weak, moderate, or strong based on the criteria.

