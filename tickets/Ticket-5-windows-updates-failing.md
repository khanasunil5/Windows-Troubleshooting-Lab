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

