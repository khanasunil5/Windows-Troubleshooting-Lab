# Printer Error – Unexpected Configuration Problem

## User-Reported Issue
User receives error stating printer has experienced an unexpected configuration problem.

## Impact
User unable to print documents.

## Environment
- Windows client
- Microsoft Print to PDF printer
- Local printer using PORTPROMPT

## Investigation
- Attempted to print and reproduced error
- Checked Print Spooler service
- Reviewed printer configuration and ports

## Findings
- Print Spooler service stopped and disabled
- Stuck print jobs present
- Printer port verified as correct

## Root Cause
Print Spooler service disabled, preventing print jobs from processing.

## Resolution
- Set Print Spooler startup type to Automatic
- Restarted Print Spooler service
- Cleared spooler cache (C:\Windows\System32\spool\PRINTERS)
- Removed and reinstalled printer
- Verified printer port configuration

## Verification
Test print completed successfully.

## Tools Used
- Services.msc
- Devices and Printers
- Event Viewer (PrintService)

## Status
Resolved
