## Objective

Install the Active Directory Domain Services (AD DS) role on the Windows Server 2025 machine in preparation for creating a domain controller.

---

## Environment

|Setting|Value|
|---|---|
|Host Platform|VMware Workstation|
|Operating System|Windows Server 2025 Standard Evaluation|
|Server Name|DC01|
|Role|Future Domain Controller|

---

## Procedure

### Open Add Roles and Features Wizard

Server Manager → Manage → Add Roles and Features

---

### Installation Type

Selected:

Role-based or feature-based installation

---

### Server Selection

Target Server:

DC01

---

### Server Roles

Enabled:

- Active Directory Domain Services (AD DS)
    

Additional features required by AD DS were accepted automatically.

---

### Features

No additional features were selected.

---

### Confirmation

Enabled:

- Restart the destination server automatically if required.
    

Installation was started.

---

## Installed Components

- Active Directory Domain Services
    
- Group Policy Management
    
- AD DS Tools
    
- Active Directory PowerShell Module
    
- Active Directory Administrative Center
    
- AD DS Snap-ins and Command-Line Tools
    

---

## Result

The Active Directory Domain Services role was installed successfully.

The server became eligible for promotion to a domain controller.

---

## Screenshot

![[Installing-ADDS.png]]

---

## What I Learned

- Active Directory is installed as a server role.
    
- Installing AD DS alone does not create a domain controller.
    
- Additional management tools are automatically installed alongside AD DS.