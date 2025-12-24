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

## Screenshots / Evidence

-[printer-added](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/1-printer-added.png)
-[spooler-disabled](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/2-spooler-disabled.png)
-[unable-to-print](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/3-unable-to-print.png)
-[spooler-running](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/4-spooler-running.png)
-[printers-folder-cleared](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/5-printers-folder-cleared.png)
-[printers-readded](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/6-printers-readded.png)
-[printers-ports](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/7-printers-ports.png)
-[successfull-print](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/bf76e472545548b76dd4c9afa94277ed5f2b3b06/evidence/ticket-4/8-successfull-print.png)

## Status
Resolved
