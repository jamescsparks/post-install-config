<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Item 1 Configure system settings and branding (Company Name, Timezone, Logo)
- Item 2 Set up departments, teams, and staff roles
- Item 3 Configure email piping or fetching via SMTP/IMAP
- Item 4 Enable and test ticket auto-responses and alerts
- Item 5 Secure and backup the osTicket installation

<h2>Configuration Steps</h2>


![EE007F68-6E55-42BF-B0FF-C2FAD96B2601](https://github.com/user-attachments/assets/9cb2783a-329d-40aa-b2f3-35e1c33c014c)
</p>

<p>
1. Access Admin Panel
Open a browser and navigate to your osTicket instance:
http://localhost/osTicket/scp
Log in with the admin credentials created during setup.
<p>
  
2. Configure Company Profile
Navigate to: Admin Panel > Settings > Company
Enter:
Help Desk Name
Default Email
Company Logo
Time Zone
Click Save Changes
<p>
<br />


![50A766F0-3355-484E-A29D-5E1F3EEDDD58_4_5005_c](https://github.com/user-attachments/assets/93fbe8f5-7d06-437e-b39d-68c1ee757334)

<p>
3. Create Departments and Assign Staff
Go to Admin Panel > Staff > Departments
Create departments like:
IT Support
Human Resources
Facilities
Assign a department manager and ticket assignment rules.
<p>
4. Set Up Teams and Roles
Go to Admin Panel > Staff > Teams
Create cross-functional teams for escalations.
Define roles under Staff > Roles with permission levels:
Agent
Manager
Admin
</p>
<br />

![184206B7-C78E-4686-ADA5-564A963D181D](https://github.com/user-attachments/assets/03f5608e-bda4-4a73-b74f-289f9d38f7a6)

</p>

<p>
5. Configure Email Integration
Navigate to Email > Emails > Add New Email
Enter the help desk email (e.g., support@domain.com)
Set SMTP/IMAP settings to enable email fetching and sending
Enable Email Fetching via Cron or Scheduled Tasks (Windows Task Scheduler or cron on Linux if applicable)
</p>
<p>
6. Configure Auto-Responses & Alerts
Under Admin Panel > Settings > Autoresponder:
Enable New Ticket auto-reply
Enable New Message auto-reply
Under Admin Panel > Settings > Alerts and Notices:
Enable alerts for new tickets, assignments, and responses
Customize messages as needed
</p>
7. Secure the Installation
Ensure /include/ost-config.php is read-only
Delete or restrict access to the /setup folder if still present
Apply Windows Firewall rules to limit access to the osTicket admin interface
Update your VM and install antivirus software (optional but recommended)
<p>

8. Backup Strategy
Export the MySQL database regularly using tools like phpMyAdmin or mysqldump
Backup the C:\inetpub\wwwroot\osTicket folder and config files
Use Azure Backup or another scheduled backup solution for the VM
</p>
<br />
