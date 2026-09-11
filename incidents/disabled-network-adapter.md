# Workstation Lost Network Connectivity

## Reported Issue

A user reported losing internet access and access to organizational
network resources. Other users were not experiencing the same problem.

## Environment

- Windows 11 Pro domain-joined workstation
- Virtual Ethernet network adapter
- Active Directory domain environment
- Organizational network resources

## Troubleshooting

Because other users remained connected, I treated the issue as likely
isolated to the affected workstation rather than a broader network
outage.

I checked the workstation's network configuration using `ipconfig /all`
and found that the expected network adapter was not present in the
active network configuration.

I then checked Device Manager and found that the workstation's Ethernet
adapter was disabled.

## Resolution

I re-enabled the network adapter in Device Manager.

The reason the adapter became disabled was not established during the
incident.

## Verification

After re-enabling the adapter, I verified that:

- Network connectivity was restored
- Internet access was functional
- Organizational network resources were accessible

## Skills Demonstrated

- Windows 11 endpoint troubleshooting
- Device Manager
- Network adapter troubleshooting
- TCP/IP troubleshooting
- Scope isolation
- Resolution verification
- Support documentation

## Key Takeaway

Determining the scope of an outage can quickly narrow troubleshooting.
Because other users remained connected, investigating the affected
workstation before assuming a network-wide problem led directly toward
the local network adapter.
