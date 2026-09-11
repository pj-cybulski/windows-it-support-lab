# Shared Printer Present but Unable to Print

## Reported Issue

A user reported that a shared network printer was installed and visible
on the workstation but would not print.

## Environment

- Windows 11 Pro domain-joined workstation
- Windows print server
- Shared network printer
- Windows Print Spooler service
- Physical network printer

## Troubleshooting

I confirmed that the expected shared printer was installed on the
workstation.

I then checked the Windows Print Spooler service and found that the
service was stopped even though its startup type was configured as
Automatic.

I attempted to start the service but did not have sufficient privileges
with my normal technician account to perform that action.

Because the Print Spooler was configured to start automatically, I
determined that restarting the workstation was an appropriate way to
restore the service without exceeding my available permissions.

## Resolution

I restarted the workstation.

After the restart, the Print Spooler service was running and printing
functionality was restored.

The incident established that the stopped Print Spooler caused the
printing failure, but it did not establish why the service had stopped.

## Verification

After the restart, I verified that:

- The Print Spooler service was running
- The shared printer remained installed
- The workstation could communicate with the printer
- A test page printed successfully

## Skills Demonstrated

- Windows 11 endpoint troubleshooting
- Network printer troubleshooting
- Windows services
- Print Spooler troubleshooting
- Shared printer support
- Technician permission boundaries
- Resolution verification
- Support documentation

## Key Takeaway

A printer being installed correctly does not mean every component
required for printing is functioning.

Checking the Windows service responsible for print processing identified
the immediate failure. The issue was resolved within the permissions
available to the technician while avoiding unsupported assumptions about
why the service had stopped.
