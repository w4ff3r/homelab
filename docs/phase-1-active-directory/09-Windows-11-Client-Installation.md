## Objective

Deploy a Windows 11 Professional client virtual machine to act as a workstation within the Active Directory environment.

---

## Environment

|Setting|Value|
|---|---|
|Virtual Machine Name|CL01|
|Operating System|Windows 11 Pro|
|RAM|4 GB|
|CPU|1 Processor, 2 Cores|
|Disk Size|80 GB|
|Network Adapter|Same VMware Network as DC01|
|Local Administrator Account|LocalAdmin|

---

## Installation Procedure

### Create Virtual Machine

A new VMware virtual machine named CL01 was created.

### Hardware Configuration

- Memory: 4 GB
    
- CPU: 1 Processor, 2 Cores
    
- Storage: 80 GB
    
- Firmware: UEFI
    
- TPM: Enabled
    

### Windows Installation

Windows 11 Pro was installed using the official Microsoft ISO.

During setup:

- Region: Australia
    
- Keyboard Layout: US
    
- Setup Type: Work or School
    
- Local Account Creation: Domain Join Instead
    

### Local Administrator Account

|Setting|Value|
|---|---|
|Username|LocalAdmin|
|Security Question Answers|LabAnswer|

---

## Result

CL01 was successfully deployed and prepared for Active Directory integration.

---

## Lessons Learned

- Windows 11 Pro is required for Active Directory domain joining.
    
- VMware encryption is required to support TPM.
    
- Local administrator accounts provide a recovery mechanism if domain authentication becomes unavailable.