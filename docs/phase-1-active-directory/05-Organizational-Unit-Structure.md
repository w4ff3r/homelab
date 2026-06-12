## Objective

Create a scalable Organizational Unit (OU) hierarchy within Active Directory to separate users, computers, servers, groups, and departments. This structure provides a foundation for future Group Policy implementation and simplifies administration.

---

## Environment

|Setting|Value|
|---|---|
|Operating System|Windows Server 2025 Standard Evaluation|
|Server Name|DC01|
|Domain Name|prestonlab.internal|
|Role|Domain Controller|

---

## Procedure

### Step 1: Open Active Directory Users and Computers

From **Server Manager**, navigate to:

```
Tools
→ Active Directory Users and Computers
```

Expand the domain:

```
prestonlab.internal
```

---

### Step 2: Create the Corporate OU

Right-click:

```
prestonlab.internal
```

Select:

```
New
→ Organizational Unit
```

Enter:

```
Corporate
```

Leave:

```
Protect container from accidental deletion
```

enabled.

Click:

```
OK
```

---

### Step 3: Create Child OUs

Right-click:

```
Corporate
```

Select:

```
New
→ Organizational Unit
```

Create the following Organizational Units:

- Users
    
- Computers
    
- Groups
    
- Servers
    
- Service Accounts
    
- Departments
    

---

### Step 4: Create Department OUs

Right-click:

```
Departments
```

Select:

```
New
→ Organizational Unit
```

Create the following department OUs:

- IT
    
- HR
    
- Finance
    
- Sales
    
- Management
    

---

## Final Structure

```
prestonlab.internal
│
├── Builtin
├── Computers
├── Domain Controllers
├── Users
│
└── Corporate
     │
     ├── Users
     ├── Computers
     ├── Groups
     ├── Servers
     ├── Service Accounts
     └── Departments
          │
          ├── IT
          ├── HR
          ├── Finance
          ├── Sales
          └── Management
```

---

## Why Organizational Units Are Important

Organizational Units provide logical separation of Active Directory objects and allow administrators to:

- Organize resources by function or department.
    
- Delegate administration to specific teams.
    
- Apply Group Policy Objects (GPOs) to selected areas of the domain.
    
- Build a scalable structure that can accommodate future growth.
    

The default **Users** and **Computers** containers provided by Active Directory are not Organizational Units and have limited Group Policy capabilities. Creating custom OUs provides greater flexibility and aligns with enterprise best practices.

---

## Result

A company-style Active Directory hierarchy was successfully implemented under the **Corporate** OU. The structure is prepared for:

- User account creation.
    
- Security group management.
    
- Computer account management.
    
- Group Policy deployment.
    
- Future expansion of the homelab.
    

![[Organisational-Units-Structure.png]]

---

## Lessons Learned

- Organizational Units are different from the default Active Directory containers.
    
- Custom OUs provide better organization and policy management.
    
- A hierarchical OU structure improves scalability and mirrors real-world enterprise environments.
    
- Separating departments will allow targeted Group Policy implementation later in the project.