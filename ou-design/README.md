# 🏢 Active Directory Organizational Unit (OU) Design & Access Management Lab

## 📌 Overview

This lab demonstrates the implementation of Organizational Units (OUs), user account management, security groups, shared folder permissions, and role-based access control within a Windows Server Active Directory environment.

The objective was to create departmental structures, manage users and groups, secure access to shared resources, and implement administrative privileges according to business and security requirements.

---

## 🎯 Objectives

- Create Organizational Units (OUs) for departmental administration
- Create and manage Active Directory user accounts
- Implement security groups for access control
- Configure shared folders and permissions
- Assign users to departmental groups
- Implement Role-Based Access Control (RBAC)
- Delegate administrative privileges securely
- Validate user authentication and authorization

---

## 🛠️ Technologies Used

- Windows Server 2022
- Active Directory Users and Computers (ADUC)
- Organizational Units (OUs)
- Active Directory Security Groups
- Shared Folder Permissions
- NTFS Permissions
- Windows Authentication
- Role-Based Access Control (RBAC)

---

# 🏢 Phase 1: Creating the Sales Organizational Unit

## Objective

Create a dedicated Organizational Unit (OU) for the Sales department to logically organize users, groups, and resources.

### Image 01 – Active Directory Users and Computers

![Image 01](screenshots/image01-aduc-console.png)

Opened Active Directory Users and Computers to begin creating the Sales organizational structure.

---

### Image 02 – Creating the Sales OU

![Image 02](screenshots/image02-create-sales-ou.png)

Created a new Organizational Unit named **Sales** to contain departmental resources and user accounts.

### Outcome

✅ Successfully created a dedicated Organizational Unit for Sales department administration.

---

# 👤 Phase 2: User Account Creation

## Objective

Create and configure user accounts within the Sales Organizational Unit.

### Image 03 – Creating a Sales User

![Image 03](screenshots/image03-create-sales-user.png)

Created a new user account within the Sales OU.

---

### Image 04 – Initial Password Configuration

![Image 04](screenshots/image04-user-password-configuration.png)

Configured the user's initial password and enforced password change at first logon to improve account security.

---

### Image 05 – User Successfully Created

![Image 05](screenshots/image05-sales-user-created.png)

The user account was successfully created within the Sales Organizational Unit.

### Outcome

✅ Successfully provisioned a departmental user account using secure onboarding practices.

---

# 👥 Phase 3: Security Group Creation

## Objective

Create a security group to manage access to Sales department resources.

### Image 06 – Creating the Sales Security Group

![Image 06](screenshots/image06-create-sales-group.png)

Created a Security Group named **Sales Group** to control access to departmental resources.

Security Groups provide centralized permission management and simplify user access administration.

### Outcome

✅ Implemented group-based access control for Sales department users.

---

# 📂 Phase 4: Shared Folder Creation and Permission Management

## Objective

Configure a shared folder that can only be accessed by authorized Sales personnel.

### Image 07 – Creating the Sales File Share

![Image 07](screenshots/image07-create-sales-folder.png)

Created a shared folder named **Sales File** on the server.

---

### Image 08 – Advanced Sharing Configuration

![Image 08](screenshots/image08-advanced-sharing.png)

Opened Advanced Sharing settings to configure network access.

---

### Image 09 – Enabling Folder Sharing

![Image 09](screenshots/image09-enable-folder-sharing.png)

Enabled network sharing and opened permission settings.

---

### Image 10 – Removing Default Permissions

![Image 10](screenshots/image10-remove-everyone-group.png)

Removed the default **Everyone** group to strengthen security and reduce unauthorized access.

---

### Image 11 – Selecting Security Principals

![Image 11](screenshots/image11-select-security-principal.png)

Opened Advanced Object Selection to locate Active Directory groups.

---

### Image 12 – Searching Active Directory Objects

![Image 12](screenshots/image12-find-sales-group.png)

Located and selected the Sales Group from Active Directory.

---

### Image 13 – Confirming Group Selection

![Image 13](screenshots/image13-confirm-sales-group.png)

Confirmed the Sales Group selection.

---

### Image 14 – Assigning Permissions

![Image 14](screenshots/image14-assign-share-permissions.png)

Assigned Change permissions to the Sales Group.

---

### Image 15 – Shared Folder Network Path

![Image 15](screenshots/image15-sales-share-path.png)

Verified the shared folder network path:

```text
\\WS2022-DC01\Sales File
```

### Outcome

✅ Successfully implemented secure file sharing using group-based permissions.

---

# 👥 Phase 5: Group Membership Management

## Objective

Grant users access to shared resources through security group membership.

### Image 16 – Adding User to Sales Group

![Image 16](screenshots/image16-add-user-to-sales-group.png)

Opened Sales Group membership settings.

---

### Image 17 – Membership Confirmation

![Image 17](screenshots/image17-sales-group-member-added.png)

Added Nomvula Teka to the Sales Group.

---

### Image 18 – User-Centric Membership Management

![Image 18](screenshots/image18-user-memberof-tab.png)

Demonstrated an alternative method of managing group memberships through user account properties.

---

### Image 19 – Existing Group Memberships

![Image 19](screenshots/image19-user-group-memberships.png)

Reviewed current group memberships assigned to the user.

---

### Image 20 – Advanced Group Search

![Image 20](screenshots/image20-group-search-advanced.png)

Opened Advanced Search for Active Directory groups.

---

### Image 21 – Active Directory Group Discovery

![Image 21](screenshots/image21-group-search-results.png)

Reviewed available groups and security principals within Active Directory.

### Outcome

✅ Successfully implemented centralized access management using security group membership.

---

# 🛡️ Phase 6: Administrative Access Delegation

## Objective

Create an ICT department structure and assign administrative privileges to a designated administrator.

### Image 22 – ICT Department Creation

![Image 22](screenshots/image22-ict-ou-user-group-created.png)

Created the ICT Organizational Unit, security group, and administrator account.

---

### Image 23 – Assigning Administrative Responsibilities

![Image 23](screenshots/image23-ict-admin-user.png)

Prepared the ICT Systems Administrator account for elevated access.

---

### Image 24 – Administrative Group Memberships

![Image 24](screenshots/image24-admin-group-memberships.png)

Assigned privileged administrative groups including:

- DHCP Administrators
- DNS Admins
- Domain Admins
- Enterprise Admins
- Hyper-V Administrators
- Protected Users
- Information Communication Technology Group

### Outcome

✅ Implemented Role-Based Access Control (RBAC) for infrastructure administration.

---

# 🔐 Phase 7: Authentication and Access Validation

## Objective

Validate administrator login and access permissions.

### Image 25 – Administrator Login

![Image 25](screenshots/image25-admin-login.png)

Attempted first sign-in using the administrator account.

---

### Image 26 – Password Change Requirement

![Image 26](screenshots/image26-password-change-required.png)

The account was required to change its password during first login.

---

### Image 27 – Password Update

![Image 27](screenshots/image27-password-update.png)

Configured a new secure password.

---

### Image 28 – Password Change Successful

![Image 28](screenshots/image28-password-changed.png)

Password update completed successfully.

---

### Image 29 – Successful Administrator Sign-In

![Image 29](screenshots/image29-admin-signin-successful.png)

Administrator account authenticated successfully.

---

### Image 30 – Accessing Shared Resources

![Image 30](screenshots/image30-access-server-share.png)

Accessed server resources through the network path.

---

### Image 31 – Access Denied Validation

![Image 31](screenshots/image31-access-denied-example.png)

Verified that users without appropriate permissions were denied access.

This demonstrates the effectiveness of access control mechanisms implemented throughout the lab.

### Outcome

✅ Successfully validated authentication, authorization, and access control policies.

---

# 🔒 Security Concepts Demonstrated

- Principle of Least Privilege (PoLP)
- Role-Based Access Control (RBAC)
- Security Group Management
- Access Control Lists (ACLs)
- Authentication & Authorization
- Organizational Unit Design
- Shared Folder Security
- Administrative Delegation

---

# 🏆 Key Achievements

✅ Designed Organizational Units for departmental management

✅ Created and managed Active Directory users and groups

✅ Configured secure shared folders and permissions

✅ Implemented Security Group-based access control

✅ Assigned administrative privileges using RBAC principles

✅ Validated authentication and authorization workflows

✅ Demonstrated secure access management within Active Directory

---


