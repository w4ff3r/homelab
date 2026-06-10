### Objective

Prepare the Windows Server 2025 machine for Active Directory Domain Services installation by assigning a static IP address.

### Environment

|Setting|Value|
|---|---|
|Host Platform|VMware Workstation|
|Operating System|Windows Server 2025 Standard Evaluation|
|Server Name|DC01|
|Role|Future Domain Controller|

### Original Network Configuration

The server initially received its network configuration through DHCP.

|Setting|Value|
|---|---|
|IP Address|192.168.237.128|
|Subnet Mask|255.255.255.0|
|Default Gateway|192.168.237.2|
|DNS Server|192.168.237.2|

### Changes Performed

The network adapter was reconfigured to use a static IPv4 address. To do this:

1. In Server Manager, under Local Server, select Ethernet0 (alternatively, go win + R and type ncpa.cpl and press Enter)
2. Right click Ethernet0 in Network Connections and select properties
3. Double click IPv4
4. Insert new configurations below

#### New Configuration

|Setting|Value|
|---|---|
|IP Address|192.168.237.128|
|Subnet Mask|255.255.255.0|
|Default Gateway|192.168.237.2|
|Preferred DNS|192.168.237.128|
|Alternate DNS|8.8.8.8|

### Reasoning

Domain Controllers should use a static IP address to ensure services such as Active Directory, DNS, and authentication remain reachable at a consistent network address.

The preferred DNS server was configured as the server's own IP address because Active Directory will install and utilise the local DNS service.

### Result

The server now uses a static IP address and is ready for Active Directory Domain Services installation.

### Testing/Troubleshooting:

Sent ping to 8.8.8.8 and google.com, both succeeded; no troubleshooting required.