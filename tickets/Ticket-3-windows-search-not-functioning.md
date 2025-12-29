# Windows Search Not Returning Results

## User-Reported Issue
User reports Windows Search opens but does not return results and shows indexing warning.

## Impact
User unable to efficiently locate applications or files.

## Environment
- Windows domain client
- Standard user account

## Investigation
- Logged in as administrator
- Checked Services console (services.msc)
- Identified Windows Search service status

## Findings
- Windows Search (WSearch) service stopped
- Startup type set to Disabled

## Root Cause
Required Windows Search service disabled, preventing indexing functionality.

## Resolution
- Set Windows Search startup type to Automatic (Delayed Start)
- Started service

## Verification
- Logged in as affected user
- Search returned results immediately
- Indexing warning no longer displayed

## Tools Used
- Services.msc

## Status
Resolved

## Screenshots / Evidence

- [service-disabled](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/e1efd5ab7cec572022a21eb05d92af282bc62778/evidence/ticket-3/1-service-disabled.png)
- [Search-indexing-off](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/e1efd5ab7cec572022a21eb05d92af282bc62778/evidence/ticket-3/2-Search-indexing%20-off.png)
- [service-properties](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/e1efd5ab7cec572022a21eb05d92af282bc62778/evidence/ticket-3/3-service-properties.png)
- [Windows-search-fixed](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/e1efd5ab7cec572022a21eb05d92af282bc62778/evidence/ticket-3/4-Windows-search-fixed.png)
- [search-working](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/e1efd5ab7cec572022a21eb05d92af282bc62778/evidence/ticket-3/5-search-working.png)
