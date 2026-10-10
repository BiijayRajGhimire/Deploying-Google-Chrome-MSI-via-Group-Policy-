# Deploying-Google-Chrome-MSI-via-Group-Policy-
Enterprise silent push to all domain-joined computers, no manual install by employees  
1.	Purpose and Scope  
This document describes how to deploy the Google Chrome Enterprise MSI package to all domain-joined Windows computers using Active Directory Group Policy (GPO Software Installation). Once complete, every targeted computer installs Chrome automatically at startup, with no user action required.  
2.	Prerequisites  
•	Active Directory domain with a working Group Policy Management Console (GPMC) on an admin workstation or domain controller.  
•	Domain admin (or delegated GPO and OU) permissions.  
•	A file server or shared folder reachable by all target computers.  
•	Target computers joined to the domain and able to reach the share at startup.  
•	Chrome Enterprise MSI (64-bit recommended): GoogleChromeStandaloneEnterprise64.msi.  
•	Chrome ADMX policy templates (optional but strongly recommended for settings control).  
3.	Step 1: Download the Chrome Enterprise Bundle  
1.	Go to the Chrome Enterprise download page (chromeenterprise.google/browser/download).  
2.	Select Windows 64-bit MSI and download the bundle.  
3.	Extract the ZIP. You will need:  
4.Installers\GoogleChromeStandaloneEnterprise64.msi  
5.Configuration\admx\ (policy templates, including chrome.admx, google.admx, and language folders such as en-US)
<img width="190" height="234" alt="image" src="https://github.com/user-attachments/assets/86feed85-11eb-477f-b78f-cf27ddab18be" />
After Active Directory domain with a working Group Policy Management Console  
(GPMC) on an admin workstation or domain controller and move pc to employee department
<img width="975" height="421" alt="image" src="https://github.com/user-attachments/assets/3323ad1c-498e-4712-9d33-07f438d335bf" />
A file server or shared folder reachable by all target computers.
<img width="890" height="316" alt="image" src="https://github.com/user-attachments/assets/179251b0-8556-4691-af13-846f4fecf63a" />
<img width="975" height="387" alt="image" src="https://github.com/user-attachments/assets/6a6bf3b0-b991-4367-be95-cd4d25630dd5" />
<img width="463" height="305" alt="image" src="https://github.com/user-attachments/assets/3ed55bd0-25de-40ba-966f-e87514a16e8a" />
After Go to group policy and choose Default domain controller edit by right click.  
Then choose computer configuration/policies/software setting.  
<img width="975" height="405" alt="image" src="https://github.com/user-attachments/assets/0b59ba60-9562-43bb-875e-39cd42f35b38" />
<img width="827" height="416" alt="image" src="https://github.com/user-attachments/assets/c24a0eaa-2ed0-499b-8218-8e5d3180a39b" />
<img width="975" height="321" alt="image" src="https://github.com/user-attachments/assets/eebb3788-16cd-4aac-8777-90a639637c88" />
Ater Add chrome Msi software file need to gpupdate /force through cmd  
<img width="975" height="201" alt="image" src="https://github.com/user-attachments/assets/cea5ba36-d1e6-4b3e-8938-c92fd0806cad" />
After process check policy could work or not?
<img width="975" height="494" alt="image" src="https://github.com/user-attachments/assets/9b9df443-6ca5-432e-8281-075b233fd35d" />


