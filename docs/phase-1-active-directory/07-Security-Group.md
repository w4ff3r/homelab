## Objective

Create Active Directory security groups and assign users based on their job roles and departments. This implements Role-Based Access Control (RBAC) and establishes a scalable permissions model.

---

## Environment

|Setting|Value|
|---|---|
|Domain|prestonlab.internal|
|Server|DC01|
|Tool|Active Directory Users and Computers|
|Group Scope|Global|
|Group Type|Security|

---

## Naming Convention

Security groups were named using the following format:

```text
GG_<Department or Role>
```

Where:

- GG = Global Group
    

Examples:

- GG_IT_Admins
    
- GG_IT_Helpdesk
    
- GG_HR
    
- GG_Finance
    
- GG_Sales
    
- GG_Management
    

This naming convention improves consistency and makes group purposes easily identifiable.

---

## Procedure

### Step 1: Open Active Directory Users and Computers

Navigate to:

Server Manager

→ Tools

→ Active Directory Users and Computers

---

### Step 2: Navigate to the Groups OU

Expand:

prestonlab.internal

→ Corporate

→ Groups

---

### Step 3: Create New Groups

Right-click:

Groups

→ New

→ Group

For each group:

- Group Scope: Global
    
- Group Type: Security
    

---

### Step 4: Create Security Groups

The following groups were created:

|Group Name|Purpose|
|---|---|
|GG_IT_Admins|IT administrators|
|GG_IT_Helpdesk|Help desk staff|
|GG_HR|Human Resources|
|GG_Finance|Finance staff|
|GG_Sales|Sales staff|
|GG_Management|Management staff|

---

### Step 5: Assign Users to Groups

Users were added to the appropriate groups through the Members tab.

---

## Group Membership

### GG_IT_Admins

|User|
|---|
|Jacob Preston|

### GG_IT_Helpdesk

|User|
|---|
|HelpDesk Account|

### GG_HR

|User|
|---|
|Sarah Johnson|

### GG_Finance

|User|
|---|
|Michael Brown|

### GG_Sales

|User|
|---|
|Emma Wilson|

### GG_Management

|User|
|---|
|David Smith|

---

## Active Directory Structure

```text
prestonlab.internal
│
└── Corporate
     │
     ├── Departments
     │
     │    IT
     │      Jacob Preston
     │      HelpDesk Account
     │
     │    HR
     │      Sarah Johnson
     │
     │    Finance
     │      Michael Brown
     │
     │    Sales
     │      Emma Wilson
     │
     │    Management
     │      David Smith
     │
     └── Groups
          │
          GG_IT_Admins
          GG_IT_Helpdesk
          GG_HR
          GG_Finance
          GG_Sales
          GG_Management
```

---

## Why Use Security Groups?

Permissions should be assigned to groups rather than individual users.

For example, instead of granting access directly to:

- Michael Brown
    

access would be granted to:

- GG_Finance
    

Any future Finance employees would inherit permissions automatically by becoming members of GG_Finance.

This approach simplifies administration and follows the principle of Role-Based Access Control (RBAC).

---

## Result

Security groups were successfully created and populated with users according to their departmental roles.

This structure provides a foundation for:

- File permissions
    
- Shared folders
    
- Printer access
    
- Group Policy Objects
    
- Delegated administration
    
- Future expansion of the domain
    

---

## Screenshots

| Screenshot                       | Description                      |
| -------------------------------- | -------------------------------- |
| ![[Security-Groups-Created.png]] | Security groups created          |
| ![[User-Added-To-Group.png]]     | Example membership configuration |


---

## Lessons Learned

- Users should receive permissions through group membership rather than individually.
    
- Security groups simplify administration and improve scalability.
    
- Global Security Groups are commonly used for departmental access control.
    
- Role-Based Access Control (RBAC) reduces management complexity and aligns with enterprise best practices.

---

## Portfolio Reflection

This stage introduced the concept of Role-Based Access Control (RBAC) within Active Directory. Rather than assigning permissions directly to users, I implemented Global Security Groups to represent job roles and departments.

This design improves scalability and reflects common enterprise practices, where permissions are managed through groups instead of individual accounts. Through this process, I developed experience with group scopes, group membership, and Active Directory access management principles.