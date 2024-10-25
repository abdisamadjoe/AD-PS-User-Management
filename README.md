# Active Directory & User Management with PowerShell (Homelab) Walkthrough
## Description
This project is a Python-based tool that assesses the complexity of passwords. It evaluates the strength of a password based on criteria such as length, presence of uppercase and lowercase letters, numbers, and special characters. The tool then provides feedback, classifying the password as strong, moderate, or weak based on the criteria met.

## Languages and Utilities Used

- **Python**

## Environments Used 

- **Windows 11**
- **Visual Studio Code**

## Project Walkthrough:

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

