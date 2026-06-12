## Objective

Create user accounts within Active Directory and organize them according to their respective departments. This provides the foundation for role-based access control and future Group Policy implementation.

---

## Environment

|Setting|Value|
|---|---|
|Domain|prestonlab.internal|
|Server|DC01|
|Role|Domain Controller|
|Active Directory Tool|Active Directory Users and Computers|

---

## Naming Convention

Usernames were created using the following convention:

```text
First Initial + Surname
```

Examples:

|Name|Username|
|---|---|
|Jacob Preston|jpreston|
|Sarah Johnson|sjohnson|
|Michael Brown|mbrown|

This naming convention is commonly used within enterprise environments because it provides a predictable and scalable method for user identification.

---

## Procedure

### Step 1: Open Active Directory Users and Computers

Navigate to:

```text
Server Manager
→ Tools
→ Active Directory Users and Computers
```

---

### Step 2: Navigate to Department OU

Example:

```text
prestonlab.internal
└── Corporate
     └── Departments
          └── IT
```

---

### Step 3: Create a New User

Right-click the department OU and select:

```text
New
→ User
```

Complete the following fields:

- First Name
    
- Last Name
    
- User Logon Name
    

---

### Step 4: Configure Password

For lab purposes:

- User must change password at next logon: Disabled
    
- Password never expires: Enabled
    

---

### Step 5: Repeat for Remaining Departments

The process was repeated for each department OU.

---

## User Accounts Created

### IT Department

|Full Name|Username|
|---|---|
|Jacob Preston|jpreston|
|HelpDesk Account|helpdesk01|

### HR Department

|Full Name|Username|
|---|---|
|Sarah Johnson|sjohnson|

### Finance Department

|Full Name|Username|
|---|---|
|Michael Brown|mbrown|

### Sales Department

|Full Name|Username|
|---|---|
|Emma Wilson|ewilson|

### Management Department

|Full Name|Username|
|---|---|
|David Smith|dsmith|

---

## Active Directory Structure

```text
prestonlab.internal
└── Corporate
     └── Departments
          ├── IT
          │
          │  Jacob Preston
          │  HelpDesk Account
          │
          ├── HR
          │  Sarah Johnson
          │
          ├── Finance
          │  Michael Brown
          │
          ├── Sales
          │  Emma Wilson
          │
          └── Management
             David Smith
```

---

## Result

User accounts were successfully created and organized according to departmental Organizational Units.

This structure establishes a foundation for:

- Security Groups
    
- Group Policy
    
- File Permissions
    
- Access Control
    
- Workstation Logons
    

---

## Screenshots

| Screenshot                     | Description          |
| ------------------------------ | -------------------- |
| ![[User-Creation-Tab.png]]     | User creation wizard |
| ![[IT-Users-Created.png\|428]] | IT department users  |


---

## Lessons Learned

- Active Directory user accounts are created inside Organizational Units.
    
- Naming conventions improve consistency and simplify administration.
    
- Separating users by department makes future permission management easier.
    
- User accounts are typically granted permissions through group membership rather than individually.

---

## Portfolio Reflection

This stage introduced the process of creating and organizing user accounts within Active Directory. I implemented a consistent naming convention and separated users by department to mirror common enterprise practices.

Through this process, I gained experience using Active Directory Users and Computers and developed an understanding of how user objects are structured within Organizational Units. This design will support future tasks involving security groups, Group Policy Objects, and access management.