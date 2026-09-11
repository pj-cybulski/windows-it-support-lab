# Network Shares Unavailable Despite Normal Network Connectivity

## Reported Issue

A user reported that mapped organizational network drives were visible
but could not be accessed.

Internet access remained functional.

## Environment

- Windows 11 Pro domain-joined workstation
- Active Directory domain environment
- SMB network shares
- Windows Defender Firewall
- Organizational file server resources

## Troubleshooting

I confirmed that the workstation had general network connectivity and
could communicate with the server.

DNS resolution was functioning correctly, but the mapped network drives
remained inaccessible.

Because basic connectivity and name resolution were working, I tested
the specific service required for Windows file sharing rather than
assuming that successful network communication meant the server was
fully reachable.

Using `Test-NetConnection`, I tested TCP port 445 to the server and
found that the SMB connection was failing.

I then inspected the workstation's firewall configuration and found an
outbound rule blocking TCP port 445 traffic to the server.

## Resolution

I disabled the firewall rule and restored SMB connectivity.

Because the reason for the unexpected rule was not established, I did
not assume that the issue was simply an accidental configuration
change. The condition warranted additional review outside the scope of
the immediate user-support resolution.

## Verification

After disabling the rule, I verified that:

- TCP port 445 connectivity to the server was restored
- The mapped network drives were accessible
- The user could access organizational files normally
- General network connectivity remained functional

The unexplained firewall configuration was documented for escalation
and additional investigation.

## Skills Demonstrated

- Windows 11 troubleshooting
- SMB connectivity troubleshooting
- TCP port testing
- `Test-NetConnection`
- Windows Defender Firewall
- Network scope isolation
- Mapped drive troubleshooting
- Resolution verification
- Escalation judgment
- Support documentation

## Key Takeaway

Successful ping, DNS resolution, and internet connectivity do not prove
that a specific network service is reachable. Testing the port used by
the affected service can help distinguish general connectivity from a
service-specific failure.

Restoring user functionality also does not eliminate the need to
escalate an unexpected configuration when its origin cannot be
established.
