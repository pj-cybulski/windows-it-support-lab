# Windows IT Support Lab

Hands-on Windows support environment used to practice realistic endpoint troubleshooting, Active Directory user support, Group Policy troubleshooting, shared resources, printing, client networking, documentation, and escalation in a simulated organizational setting.

## Purpose

This lab was created to build and reinforce practical IT support skills through realistic support scenarios rather than infrastructure design for its own sake.

The focus is on supporting users and Windows workstations inside an existing managed environment, including:

- Windows 11 endpoint troubleshooting
- Active Directory user and computer support
- Password resets, account status, and group membership
- Group Policy troubleshooting from domain-joined clients
- Shared folders, drive mappings, access, and permissions
- Network printing and print-related troubleshooting
- TCP/IP, DNS, DHCP, and connectivity troubleshooting
- Windows services, startup, applications, drivers, and peripherals
- Ticket documentation, verification, and appropriate escalation

## Lab Environment

The environment includes:

- Windows Server 2022 domain controller
- Active Directory Domain Services
- DNS
- Windows 11 Pro domain-joined workstations
- Technician and standard-user accounts
- Role-based security groups and permissions
- Group Policy
- Shared network resources
- Windows print services
- Physical network printer
- Virtualized lab infrastructure

The lab is intentionally presented here as a generic organizational environment and is not intended to represent the internal systems or architecture of any real organization.

## Training Method

Support incidents are introduced into the lab as controlled troubleshooting scenarios.

During an exercise, the reported symptom is presented without revealing the underlying cause. I then work through the issue using normal support and diagnostic methods, document the evidence gathered, determine and implement an appropriate resolution when possible, verify functionality, and escalate when the issue falls outside the technician role or requires additional investigation.

AI tools are used to assist with lab infrastructure, scenario preparation, and documentation. Troubleshooting decisions, diagnostic steps, resolutions, verification, and escalation decisions documented in this portfolio reflect my own work during the exercises.

## Selected Support Incidents

### [Domain Resources Unavailable While Internet Remained Functional](incidents/dns-domain-resource-access.md)

Diagnosed a domain-joined Windows 11 workstation that retained internet
connectivity while losing access to mapped organizational resources.
Isolated the problem to incorrect client DNS configuration, corrected
the configuration, and verified restored resource access.

**Skills:** Windows 11 · DNS · Domain Resources · Mapped Drives ·
Network Troubleshooting · Verification

Additional support incidents will be added as training continues.

## Portfolio Status

This portfolio is an active record of ongoing hands-on Windows IT support training. Additional incidents will be added as they are completed and reviewed.
