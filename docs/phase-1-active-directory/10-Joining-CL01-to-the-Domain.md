## Objective

Join the Windows 11 client workstation CL01 to the Active Directory domain.

---

## Domain Information

|Setting|Value|
|---|---|
|Domain Name|prestonlab.internal|
|Domain Controller|DC01|
|DNS Server|192.168.237.128|

---

## Procedure

### Configure DNS

The preferred DNS server on CL01 was configured to:

192.168.237.128

to ensure domain resources could be resolved.

---

### Verify Name Resolution

Commands used:

ping dc01

nslookup prestonlab.internal

nslookup dc01

Successful responses confirmed DNS functionality.

---

### Open System Properties

Command used:

sysdm.cpl

---

### Change Membership

Under:

Computer Name → Change

the computer was joined to:

prestonlab.internal

---

### Authentication

The following credentials were used:

[administrator@prestonlab.internal](mailto:administrator@prestonlab.internal)

The join operation completed successfully.

---

### Restart

CL01 was restarted to finalize domain membership.

---

### Domain Logon

After reboot, domain users became available for authentication.

Example:

[jpreston@prestonlab.internal](mailto:jpreston@prestonlab.internal)

---

## Result

CL01 successfully joined the Active Directory domain.

The environment now consists of:

- DC01 (Domain Controller)
    
- CL01 (Domain Client)
    

forming a functional two-machine Active Directory environment.

---

## Lessons Learned

- DNS is critical to Active Directory operations.
    
- Domain membership relies on successful name resolution.
    
- System Properties can be accessed quickly using sysdm.cpl.
    
- User authentication in Active Directory can be performed using User Principal Names (UPNs).