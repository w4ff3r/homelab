## Objective

Deploy Home Assistant OS inside VMware Workstation Pro to create a development environment for the Home Cinema Automation project before migrating to dedicated hardware.

---

## Environment

| Component | Value |
|------------|------|
| Hypervisor | VMware Workstation Pro |
| VM Name | HA01 |
| Guest Operating System | Home Assistant OS |
| CPU | 2 Processors, 2 Cores Each |
| Memory | 4 GB |
| Network | Bridged |
| Storage | Existing Home Assistant VMDK |
| Access Port | 8123 |

---

## Purpose

The Home Assistant virtual machine provides:

- A development environment
- Dashboard testing
- Plex integration testing
- Automation development
- Validation before deploying to dedicated hardware

Final deployment hardware:

- Home Assistant Green (Preferred)
- Raspberry Pi 5 (Alternative)

---

## Download Home Assistant OS

Official installation guide:

https://www.home-assistant.io/installation/windows

Download:

haos_ova-XX.x.vmdk.xz

---

## Extract Image

Install:

https://www.7-zip.org/

Extract:

haos_ova-XX.x.vmdk

---

## Create Virtual Machine

### New Virtual Machine

Create a custom virtual machine.

---

### Operating System Installation

Select:

I will install the operating system later

---

### Guest Operating System

Type:

Linux

Version:

Other Linux 6.x kernel 64-bit

---

### Virtual Machine Name

VM Name:

HA01

Location:

D:\VM\HA01

---

## Resource Allocation

### CPU

2 processors

2 cores per processor

Total:

4 vCPUs

---

### Memory

4096 MB

---

### Network

Bridged

This allows Home Assistant to obtain its own IP address and behave like a separate device on the network.

---

## Disk Configuration

Select:

Do not create a disk

The Home Assistant image will be attached manually.

---

## Attach Existing Disk

Open:

VM Settings

Remove:

- Printer
- Floppy Drive
- CD/DVD

Add:

Hard Disk → Use Existing Disk

Select:

haos_ova-XX.x.vmdk

---

## Initial Boot

Power on the virtual machine.

Home Assistant will initialize and eventually display:

http://homeassistant.local:8123

or
```html
http://<IP Address>:8123
```

---

## Verification

From another device or the host computer, open:

http://homeassistant.local:8123

Confirm that the Home Assistant setup wizard appears.

---

## Next Phase

Phase 1:

Initial configuration

Phase 2:

Plex integration

Phase 3:

Dashboard design

Phase 4:

Automation

Phase 5:

Hardware deployment