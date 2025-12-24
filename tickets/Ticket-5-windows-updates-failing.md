# Windows Updates Failing to Install

## User-Reported Issue
Windows Updates fail to install or remain stuck during checking process.

## Impact
System missing critical updates and security patches.

## Environment
- Windows domain client (CLIENT01)
- Administrator access

## Investigation
- Attempted to run Windows Update
- Checked Windows Update and BITS services
- Observed services stopped and disabled

## Findings
- Windows Update service stopped
- Background Intelligent Transfer Service (BITS) stopped

## Root Cause
Update-related services disabled, preventing update process.

## Resolution
- Set Windows Update and BITS services to Automatic
- Restarted both services
- Reset Windows Update components by clearing SoftwareDistribution\Download

## Verification
Updates successfully downloaded and installed.

## Tools Used
- Services.msc
- Command Prompt
- Windows Settings

## Status
Resolved

## Screenshots / Evidence
- [windows-update-stopped](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/1-windows-update-stopped.png)
- [BITS-stopped](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/2-BITS-stopped.png)
- [update-error](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/3-update-error.png)
- [Windows-Event-Viewer](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/4-Windows-Event-Viewer.png)
- [services-confirmed-stopped](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/5-services-confirmed-stopped.png)
- [services-started](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/6-services-started.png)
- [reset-cmd](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/dea76b1f9554def16eaec1a72cbf2a622fa73b5b/evidence/ticket-5/7-reset-cmd.png)
