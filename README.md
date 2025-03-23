# Microsoft-Azure-Security-Role-Based-Access-Control-Lab

![Azure](https://github.com/user-attachments/assets/9441ba71-f28c-48e0-814b-d3f8b45e937b)

### Objectives
- Built and documented a hands-on lab using Microsoft Entra ID (formerly Azure AD) to create and manage user identities, security groups, and role assignments—demonstrating core identity and access management skills in a cloud-based environment.

 ### Skills Learned
- Identity and Access Management (IAM) fundamentals  
- User provisioning and account creation in Microsoft Entra ID  
- Group creation and permission assignment  
- Role-based access control (RBAC) setup  
- Navigating and using the Azure Portal effectively  
- Understanding cloud-based vs. on-prem Active Directory  
- Hands-on experience with Microsoft Entra ID (formerly Azure Active Directory)  
- Secure access and user management best practices
- 
### Why Companies Use Microsoft Entra ID (Azure Active Directory)


Microsoft Entra ID (formerly Azure Active Directory) is a cloud-based identity and access management (IAM) service that helps organizations securely manage user accounts, groups, and access to company resources. 

In this example lab, you’ll see how I created a user account and assigned it to a group called "Senior Adminstrator." This group-based approach allows IT teams to manage access in a simple, organized way. Instead of setting permissions for every individual user, permissions are set at the group level and automatically applied to all group members.

This mirrors how real-world organizations manage employees, contractors, and administrators. In this instance,Nathan Johnson is in the senior adminstrator group and has special access to internal tools, reports, or configurations — and users added to that group instantly receive those permissions.

By walking through this lab, you’ll gain a better understanding of how identity is managed in cloud environment
Microsoft Entra ID (formerly Azure Active Directory) is widely used by organizations to manage identity and access in a secure and scalable way. Here are the key reasons why it's essential in modern IT environments:

-  **Centralized User Management**  
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
  Works out of the box with Microsoft 365, Teams, SharePoint, and thousands of third-party apps.

In this lab, I will show how users and groups are created vin Microsoft Azure environments.Identity and Access are at the core of how Role-Based Access Control (RBAC) works in Microsoft Azure.

In Azure; an identity can include a user, a group, and a service principal.

For instance, I created my own fictional IT company located in Cncinnati, Ohio called TigerSpeedTechnologies. We just hired an IT Support Services Director named Nathan Johnson. 

In the screenshow below, I demonstrate adding him to become a user for the company TigerspeedTechnologoies.

Additionally, I helped the IT director with his first day login process into the computer as well. I set a temporary password for him to sign into the computer then change it to a permanent secure password. =

![Nathan Johndon part 2](https://github.com/user-attachments/assets/21402348-9de1-441c-90b4-d6c32690c3b4)
**Nathan johnson Login Credentials**
Next, I added Nathan Johnson to a Senior Adminstrator group and made changes to the systems to make him the group owner.
![image](https://github.com/user-attachments/assets/17ec4a6c-a822-4171-8867-e0b39c9c268b)
**Senior Adminstrator**

From that exercise, I learned how to manage user identities and organize access using Microsoft Entra ID in the Azure portal. I created a user account from scratch and added that user to a security group, which taught me how companies can efficiently control access to resources. 

I saw how using groups makes it easier to manage roles and permissions for multiple users at once, instead of individually.

It also showed me how access can be structured securely and clearly, which is important in protecting company data. Overall, I learned the importance of centralized identity and access management in keeping IT systems organized and secure.


+++
![image](https://github.com/user-attachments/assets/f8c3d80a-c281-4f8b-a2c4-9e087a275c2d)

You used the Azure Portal to create a user and a group, and assigned the user to the group.
