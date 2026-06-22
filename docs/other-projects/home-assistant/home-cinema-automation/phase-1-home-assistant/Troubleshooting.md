## Boot Error - No Operating System Found

### Problem

The Home Assistant virtual machine failed to boot and displayed:

```text
No operating system found
```

---

### Explanation

The VM was configured to use legacy BIOS firmware. Home Assistant OS expects a UEFI boot environment and was unable to locate a valid boot loader.

---

### Solution

Changed the firmware type in VMware:

```text
VM Settings
→ Options
→ Advanced
→ Firmware Type
```

from:

```text
BIOS
```

to:

```text
UEFI
```

---

### Justification

Using UEFI aligns the virtual machine with Home Assistant OS requirements and allows the system to boot correctly. UEFI also more closely reflects modern hardware and the intended production deployment environment.

---

## Home Assistant Networking Issue

### Problem

Home Assistant booted successfully but reported no network connection and could not obtain an IP address.

### Explanation

VMware Workstation was missing the VMnet0 virtual network, preventing bridged networking from functioning and causing the VM to have no network interface.

### Solution

Opened the Virtual Network Editor with administrator privileges and restored the default network configuration. This recreated VMnet0 (Bridged), VMnet1 (Host-only), and VMnet8 (NAT).

### Justification

Restoring the default VMware network configuration re-enabled bridged networking, allowing Home Assistant to obtain an IP address and communicate with devices on the local network.

---

## Home Assistant Network Connectivity Failure

### Problem

Home Assistant booted successfully but failed to obtain an IP address and displayed:

```text
IPv4 addresses for enp2s1: (No address)
```

### Explanation

VMware VMnet0 was configured for automatic bridging, causing VMware to select an incorrect network adapter.

### Solution

Changed VMnet0 from:

```text
Bridged to: Automatic
```

to the host's physical network adapter:

```text
Intel Wi-Fi 6E
```

### Justification

Manually selecting the physical network adapter ensures that bridged virtual machines can communicate with the local network and receive IP addresses through DHCP.