
## Purpose:

This section outlines any troubleshooting that was necessary during the phase 1 process.

---
## VMware SATA Device Error

### Issue

Upon starting the virtual machine, VMware displayed:

"Cannot connect the virtual device sata0:1 because no corresponding device is available on the host."

### Cause

The virtual DVD drive was configured to connect to the Windows Server installation ISO, which was no longer present.

### Resolution

Selected:

"No"

when prompted to reconnect the device at startup.

The server booted normally.

### Result

The issue had no impact on server functionality.

Future corrective action:

Disable "Connect at power on" for the CD/DVD device.

### Lessons Learned

Virtual machines may retain references to installation media after operating system installation has completed.

---
