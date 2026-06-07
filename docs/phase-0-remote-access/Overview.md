
## Objective:

The objective of this phase was to establish remote access to my home desktop from my laptop regardless of whether I was connected to the same network. Since my desktop would be the primary "server" of the homelab, I would like the possibility of working on it when I'm not sitting at the environment.

## Technologies Used:

- [[Tailscale]]
- [[Rustdesk]]
- Windows 11 Home

## Implementation:

The primary focus was finding the right remote desktop application, which was chosen as RustDesk, before looking into the issue of off-network access. Once remote desktop within the same network was connected, I could then focus on multi-network remote access.

Initially, I considered port forwarding, however this, without the proper implementation, would leave ports open to the public, leaving my home network vulnerable. As such, I went with Tailscale for its ease simple, intuitive implementation which allowed me access to my host machine.

## Outcome:

The remote access solution was successfully implemented and tested. The laptop can now access the desktop securely through the use of Tailscale and RustDesk. This will act as my foundation for mine and my homelab's future development.

## Skills Developed:

- Remote Access Configuration
- VPN and secure networking concepts
- Device-to-device connectivity
- Remote desktop administration
- Basic troubleshooting and connectivity testing

## Next Steps:

The next phase (Phase 1) will focus on setting up the virtual machine, installing Windows Server 2025 and configuring Active Directory Domain Services, as well as user and group configuration.