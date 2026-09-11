# Domain Resources Unavailable While Internet Remained Functional

## Reported Issue

A user reported that internet access was working, but organizational
network drives were unavailable.

Because the workstation could still access the internet, general network
connectivity appeared to be functioning.

## Environment

- Windows 11 Pro domain-joined workstation
- Active Directory domain environment
- Mapped organizational network drives
- Internal DNS provided by the domain controller

## Troubleshooting

I confirmed that the workstation still had general network connectivity
while access to organizational resources was affected.

After the user signed out and back in, the expected mapped drives were
no longer available.

I checked the workstation's network configuration and found that its DNS
settings were not pointing to the domain DNS server.

In an Active Directory environment, DNS is required for clients to locate
domain services and resources. This explained why the workstation could
access the internet while still experiencing failures with domain resources.

## Resolution

I corrected the workstation's DNS configuration to use the domain DNS
server and restarted the workstation.

## Verification

After restart, I verified that:

- The expected mapped drives were available
- The user could access the drives
- Read/write access functioned normally
- General internet connectivity remained functional

## Skills Demonstrated

- Windows 11 network troubleshooting
- DNS troubleshooting
- Domain resource troubleshooting
- Mapped drive verification
- Scope isolation
- Resolution verification
- Support documentation

## Key Takeaway

Working internet access does not necessarily mean a domain-joined
workstation has correct network configuration. Incorrect DNS settings
can allow general internet connectivity while preventing proper access
to domain services and organizational resources.
