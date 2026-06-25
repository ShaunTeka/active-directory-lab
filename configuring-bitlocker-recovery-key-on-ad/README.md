
# 🔐 Configuring BitLocker Recovery Keys in Active Directory

## 📖 Overview

This lab demonstrates how to configure **Active Directory Domain Services (AD DS)** to securely store and manage **BitLocker Recovery Keys**. The objective was to enable centralized recovery key management, configure Group Policy settings for BitLocker, and validate policy deployment on a Windows 10 client machine.

Storing BitLocker Recovery Keys in Active Directory improves security, simplifies recovery processes, and ensures compliance with enterprise security standards.

---

# 🛠️ Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Group Policy Management (GPM)
- BitLocker Drive Encryption
- Windows 10 Client
- VirtualBox

---

# 🎯 Objectives

- Install BitLocker administration tools
- Enable BitLocker Recovery Key Viewer
- Configure Group Policy for BitLocker recovery
- Store recovery keys in Active Directory
- Configure operating system drive encryption
- Apply BitLocker policies through Group Policy
- Validate policy deployment on client devices

---

# 🧪 Lab Activities

## 1️⃣ Verifying BitLocker Recovery Support

Opened Active Directory Users and Computers to verify whether BitLocker Recovery information was available for a domain-joined computer.

### Activities Performed

- Opened **Server Manager**
- Selected **Tools**
- Opened **Active Directory Users and Computers**
- Navigated to the target computer object

### 📸 Screenshot

![BitLocker Tab Check](./screenshots/01-bitlocker-tab-check.png)

---

## 2️⃣ Installing BitLocker Features

Added the required BitLocker management components.

### Features Installed

- BitLocker Drive Encryption Administration Utilities
- BitLocker Recovery Password Viewer

### 📸 Screenshot

![Add Roles and Features](./screenshots/02-add-roles-features.png)

---

## 3️⃣ Selecting BitLocker Components

Configured feature selections required for Active Directory integration.

### 📸 Screenshot

![BitLocker Features](./screenshots/03-bitlocker-features.png)

---

## 4️⃣ Installing Features

Started the installation process.

### 📸 Screenshot

![Install Features](./screenshots/04-install-features.png)

---

## 5️⃣ Installation Completed

Verified successful installation.

### 📸 Screenshot

![Installation Complete](./screenshots/05-installation-complete.png)

---

## 6️⃣ Verifying BitLocker Recovery Tab

Returned to Active Directory Users and Computers and confirmed that the BitLocker Recovery tab was available.

### Observation

The message:

> "There are no items in this view"

indicated that the computer had not yet been encrypted using BitLocker.

### 📸 Screenshot

![Recovery Tab Available](./screenshots/06-recovery-tab.png)

---

# ⚙️ Group Policy Configuration

## 7️⃣ Creating a BitLocker GPO

Created a new Group Policy Object named:

**SMT BitLocker Recovery Key GPO**

### 📸 Screenshot

![Create BitLocker GPO](./screenshots/07-create-gpo.png)

---

## 8️⃣ Editing the GPO

Opened Group Policy Editor and navigated to:

```text
Computer Configuration
 └── Policies
      └── Administrative Templates
           └── Windows Components
                └── BitLocker Drive Encryption
```

### 📸 Screenshot

![Edit BitLocker GPO](./screenshots/08-edit-gpo.png)

---

## 9️⃣ Configuring Recovery Information Storage

Enabled:

**Store BitLocker Recovery Information in Active Directory Domain Services**

### Configuration Applied

✅ Enabled

✅ Require BitLocker backup to AD DS

### 📸 Screenshot

![Store Recovery Information](./screenshots/09-store-recovery-info.png)

---

## 🔟 Enabling Recovery Key Backup

Configured automatic backup of recovery keys to Active Directory.

### 📸 Screenshot

![Backup to AD DS](./screenshots/10-backup-ad-ds.png)

---

## 1️⃣1️⃣ Configuring Operating System Drives

Navigated to:

```text
BitLocker Drive Encryption
 └── Operating System Drives
```

### 📸 Screenshot

![Operating System Drives](./screenshots/11-os-drives.png)

---

## 1️⃣2️⃣ Allowing BitLocker Without TPM

Enabled:

**Require additional authentication at startup**

### Purpose

Allows BitLocker deployment on devices that do not have a Trusted Platform Module (TPM).

### 📸 Screenshot

![Additional Authentication](./screenshots/12-authentication-startup.png)

---

## 1️⃣3️⃣ TPM-Free BitLocker Support

Confirmed policy configuration.

### 📸 Screenshot

![BitLocker Without TPM](./screenshots/13-without-tpm.png)

---

## 1️⃣4️⃣ Configuring Encryption Type

Configured:

**Enforce drive encryption type on operating system drives**

### Selected Option

🔒 Used Space Only Encryption

### 📸 Screenshot

![Encryption Type](./screenshots/14-encryption-type.png)

---

## 1️⃣5️⃣ Configuring Recovery Options

Opened:

**Choose how BitLocker-protected operating system drives can be recovered**

### 📸 Screenshot

![Recovery Options](./screenshots/15-recovery-options.png)

---

## 1️⃣6️⃣ Requiring Recovery Information Storage

Enabled:

✅ Do not enable BitLocker until recovery information is stored to AD DS

### Benefit

Ensures recovery keys are securely backed up before encryption begins.

### 📸 Screenshot

![Recovery Storage Required](./screenshots/16-recovery-storage-required.png)

---

## 1️⃣7️⃣ Linking the GPO

Prepared to deploy the policy across Organizational Units (OUs).

### 📸 Screenshot

![Link GPO](./screenshots/17-link-gpo.png)

---

## 1️⃣8️⃣ Deploying to Human Resources

Linked the policy to the:

👥 Human Resources Computers OU

### 📸 Screenshot

![HR GPO Link](./screenshots/18-hr-gpo-link.png)

---

# 💻 Client Configuration

## 1️⃣9️⃣ Opening Command Prompt

Opened Command Prompt from the Run dialog.

### 📸 Screenshot

![Open CMD](./screenshots/19-open-cmd.png)

---

## 2️⃣0️⃣ Applying Group Policy

Executed:

```powershell
gpupdate /force
```

### Purpose

Refreshes and applies the latest Group Policy settings from the domain controller.

### Additional Command

```powershell
shutdown -r -t 0
```

### Purpose

Immediately restarts the client computer.

### 📸 Screenshot

![GPUpdate](./screenshots/20-gpupdate.png)

---

# 🔒 Enabling BitLocker on the Client

## 2️⃣1️⃣ Turning On BitLocker

Navigated to:

**This PC → Local Disk (C:) → Turn on BitLocker**

### 📸 Screenshot

![Enable BitLocker](./screenshots/21-enable-bitlocker.png)

---

## 2️⃣2️⃣ Verifying System Requirements

BitLocker verified that the device met the required prerequisites.

### 📸 Screenshot

![Verify Requirements](./screenshots/22-verify-requirements.png)

---

## 2️⃣3️⃣ Preparing the Drive

BitLocker prepared the operating system drive for encryption.

### 📸 Screenshot

![Prepare Drive](./screenshots/23-prepare-drive.png)

---

## 2️⃣4️⃣ Selecting Startup Authentication

Because the device does not contain a TPM chip, a startup authentication method was selected.

### 📸 Screenshot

![Startup Authentication](./screenshots/24-startup-authentication.png)

---

## 2️⃣5️⃣ Preparing Recovery Key Configuration

Configured BitLocker Recovery settings before encryption.

### 📸 Screenshot

![Recovery Preparation](./screenshots/25-recovery-preparation.png)

---

# 🚀 Skills Demonstrated

- Active Directory Administration
- BitLocker Administration
- Group Policy Management
- Endpoint Security
- Windows Server Administration
- Identity & Access Management (IAM)
- Security Hardening
- Enterprise Encryption Management
- Recovery Key Management

---

# 📚 Lessons Learned

This lab strengthened my understanding of:

- BitLocker deployment strategies
- Recovery key management
- Active Directory integration
- Group Policy administration
- Endpoint encryption
- Enterprise security controls
- Data protection best practices

---

# 🔮 Future Improvements

- BitLocker Network Unlock
- TPM-Based Deployments
- MBAM Integration
- Azure AD Recovery Key Backup
- Microsoft Intune BitLocker Management
- Endpoint Compliance Policies
- Security Baseline Configuration
- Device Encryption Monitoring

---

## ✅ Project Status

**Completed Successfully**

This project demonstrates practical experience in **BitLocker Administration**, **Active Directory Recovery Key Management**, **Group Policy Configuration**, and **Enterprise Endpoint Security** within a Windows Server environment.
````

