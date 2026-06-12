## Objective

Create Organizational Units to organize computer objects according to their purpose and prepare the Active Directory environment for future workstation and server deployments.

---

## Procedure

### Navigate to Computers OU

prestonlab.internal

→ Corporate

→ Computers

---

### Create Organizational Units

The following OUs were created:

- Workstations
    
- Laptops
    
- Test Machines

---

## Purpose

### Workstations

Stores desktop computer accounts used by employees.

### Laptops

Stores portable devices used by staff.

### Test Machines

Provides an isolated area for testing and troubleshooting.

---

## Final Structure

prestonlab.internal  
└── Corporate  
	└── Computers  
		├── Workstations  
		├── Laptops  
		├── Servers  
		└── Test Machines

---

## Result

The Active Directory structure was expanded to support future domain-joined computers and servers.

This structure prepares the environment for:

- Windows 10 clients
    
- Additional servers
    
- Group Policy Objects
    
- Computer management
    
- Testing environments
    

---

## Lessons Learned

- Computer objects should be organized into Organizational Units rather than left in the default Computers container.
    
- Organizational Units simplify administration and allow targeted Group Policy deployment.
    
- Separating workstations, laptops, and servers improves scalability and maintainability.