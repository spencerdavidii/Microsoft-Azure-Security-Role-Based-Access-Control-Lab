# Microsoft-Azure-Security-Role-Based-Access-Control-Lab

![Azure](https://github.com/user-attachments/assets/9441ba71-f28c-48e0-814b-d3f8b45e937b)

### Objectives
- Built and documented a hands-on lab using Microsoft Entra ID (formerly Azure AD) to create and manage user identities, security groups, and role assignments—demonstrating core identity and access management skills in a cloud-based environment.
- Create a Senior Admins group containing the user account of Nathan Johnson as its member.
- Create a Junior Admins group containing the user account of Aubrey Miller as its member.
- Create a Service Desk group containing the user account of Dylan Williams as its member.
 - Assign the Virtual Machine Contributor role to the Service Desk group.


 ### Skills Learned
- Identity and Access Management (IAM) fundamentals  
- User provisioning and account creation in Microsoft Entra ID  
- Group creation and permission assignment  
- Role-based access control (RBAC) setup  
- Navigating and using the Azure Portal effectively  
- Understanding cloud-based vs. on-prem Active Directory  
- Hands-on experience with Microsoft Entra ID (formerly Azure Active Directory)  
- Secure access and user management best practices

### Why Companies Use Microsoft Entra ID (Azure Active Directory)

Microsoft Entra ID (formerly Azure Active Directory) is a cloud-based identity and access management (IAM) service that helps organizations securely manage user accounts, groups, and access to company resources. 
Here a few key reasons why it is important in modern IT environments .

 **Centralized User Management**  
  Manage all user identities, roles, and access permissions from a single location—whether for 10 users or 10,000.

-  **Secure Access Control**  
  Ensure only the right people have access to the right resources, protecting sensitive data and systems.

- **Streamlined Onboarding & Offboarding**  
  Quickly assign or remove access as employees join, move departments, or leave the company.

-  **Group-Based Permissions**  
  Use security groups to assign access based on job roles, making permission management faster and more consistent.

-  **Single Sign-On (SSO)**  
  Enable users to access multiple applications with just one secure login, improving the user experience and reducing password fatigue.

-  **Remote & Hybrid Work Support**  
  Being cloud-based, Entra ID allows secure access to company resources from anywhere in the world.

-  **Compliance & Audit Trails**  
  Built-in tracking and reporting features help organizations stay compliant with industry regulations.

-  **Seamless Integration with Microsoft 365 & Cloud Apps**  
  Works out of the box with Microsoft 365, Teams, SharePoint, and

In this lab, I will show how users and groups are created vin Microsoft Azure environments.Identity and Access are at the core of how Role-Based Access Control (RBAC) works in Microsoft Azure.

In Azure; an identity can include a user, a group, and a service principal.

For instance, I created my own fictional IT company located in Cncinnati, Ohio called TigerSpeedTechnologies. We just hired an IT Support Services Director named Nathan Johnson. 

In the screenshow below, I demonstrate adding him as a member for the company TigerspeedTechnologoies.

The next day Nathan sat in his office and signed into the laptop device with his temporary password. He procced to hit control + alt + delete and changed his temporary password to a new secure password. I helped the IT director with his first day sign in process into the computer as well. I set a temporary password for him to sign into the computer then change it to a permanent secure password.

 **Nathan johnson Login Credentials**
![Nathan Johndon part 2](https://github.com/user-attachments/assets/21402348-9de1-441c-90b4-d6c32690c3b4)


Next, I added Nathan Johnson to a Senior Adminstrator group and made changes to the systems to make him the group owner.
![image](https://github.com/user-attachments/assets/17ec4a6c-a822-4171-8867-e0b39c9c268b)
**Senior Adminstrator**

From that exercise, I learned how to manage user identities and organize access using Microsoft Entra ID in the Azure portal. I created a user account from scratch and added that user to a security group, which taught me how companies can efficiently control access to resources. 

I saw how using groups makes it easier to manage roles and permissions for multiple users at once, instead of individually.

It also showed me how access can be structured securely and clearly, which is important in protecting company data. Overall, I learned the importance of centralized identity and access management in keeping IT systems organized and secure.

###Senior Admins Group Containing The User Account Of Nathan Johnson As Its Member.
Next,I created the Senior Administrators group and selected Nathan as the group owner.  ***Explain Task two from the exercise 
![image](https://github.com/user-attachments/assets/f8c3d80a-c281-4f8b-a2c4-9e087a275c2d)
**Nathan Added To The Senior Admin Group**

This group-based approach allows IT teams to manage access in a simple and organized way. Instead of setting permissions for every individual user, permissions are set at the group level and automatically applied to all group members.

This mirrors how real-world organizations manage employees, contractors, and administrators. In this instance,Nathan Johnson has special access to internal tools, reports, or configurations — and users added to that group instantly receive those permissions as well.

###Junior Admins group containing the user account of Aubrey Miller
In the second phase of the lab, I will create a junior adminstrator group and add Aubrey Miller to group. 
I will complete this process by using powershell. Essentially, powershell is a tool to use to tell the computer exactly what to do like moving programs or opening files. 

I navigated to cloud shell in the azure portal and typed **$passwordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile** to create a password profile object. 

** Reference: Password Profile Object Code**
![image](https://github.com/user-attachments/assets/90f4f037-d91f-425e-b52d-ca19fb0fbf7c)

Next, I ran the following code  **$passwordProfile.Password = "Pa55w.rd1234** to set the value of the password within the profile object.
![Azure powershell using powershel task 1](https://github.com/user-attachments/assets/92e72550-04bb-4d36-9028-71ef9b3f3543)

After I connected to Microsoft Entra ID, I typed the code  **$domainName = ((Get-AzureAdTenantDetail).VerifiedDomains)[0].Name** to identify the name of my Microsoft Entra ID Tenant.
**Microsoft Entra ID Tenant**
![Azure powershell using powershel task 1](https://github.com/user-attachments/assets/f8c5ac76-e953-403f-9a51-da049de53893)

For this phase of the lab, I selected Aubrey Miller.
I utilized this code  **New-AzureADUser -DisplayName 'Aubrey Miller' -PasswordProfile $passwordProfile -UserPrincipalName "Aubrey@$domainName" -AccountEnabled $true -MailNickName 'Aubrey'** to create a user account for Aubrey 

**Created a user account for Aubrey Miller**
![Azure powershell using powershel task 1](https://github.com/user-attachments/assets/32830def-6992-431c-9156-c44a650671c7)



+++By walking through this lab, you’ll gain a better understanding of how identity is managed in cloud environment
![image](https://github.com/user-attachments/assets/f8c3d80a-c281-4f8b-a2c4-9e087a275c2d)

You used the Azure Portal to create a user and a group, and assigned the user to the group.
