## Objective

Promote the Windows Server 2025 machine to a domain controller and create the first Active Directory forest.

---

## Environment

|Setting|Value|
|---|---|
|Server Name|DC01|
|Domain Name|prestonlab.internal|
|NetBIOS Name|PRESTONLAB|
|DNS Server|Installed locally|

---

## Procedure

### Launch Domain Controller Configuration Wizard

Server Manager → Notifications → Promote this server to a domain controller

---

### Deployment Configuration

Selected:

Add a new forest

Root Domain Name:

prestonlab.internal

---

### Domain Controller Options

Enabled:

- Domain Name System (DNS) Server
    
- Global Catalog (GC)
    

Disabled:

- Read Only Domain Controller (RODC)
    

---

### Directory Services Restore Mode

Configured a DSRM password for disaster recovery purposes.

---

### DNS Options

A warning regarding DNS delegation was displayed.

This warning was expected because no parent DNS infrastructure existed.

No action was required.

---

### NetBIOS Domain Name

Automatically generated:

PRESTONLAB

---

### Database Paths

Defaults were retained:

Database:

C:\Windows\NTDS

Logs:

C:\Windows\NTDS

SYSVOL:

C:\Windows\SYSVOL

---

### Prerequisite Checks

All prerequisite checks completed successfully.

---

### Installation

The promotion process:

1. Installed DNS.
    
2. Created the Active Directory forest.
    
3. Created the domain.
    
4. Configured SYSVOL replication.
    
5. Promoted DC01 to a Domain Controller.
    

The server automatically rebooted.

---

## Result

A new Active Directory forest named:

prestonlab.internal

was successfully created.

DC01 became the first domain controller in the environment.

---

## Screenshots

![[ADDS-Configuration-Prerequisites-Passed.png]]

---

## What I Learned

- A forest is the top-level container in Active Directory.
    
- DNS is tightly integrated with Active Directory.
    
- The Global Catalog allows directory-wide searches.
    
- DNS delegation warnings are expected in standalone lab environments.