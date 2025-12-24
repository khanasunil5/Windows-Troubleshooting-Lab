## Corrupted Windows User Profile (Temporary Profile Issue)

## User-Reported Issue
User reports logging in successfully but receives a temporary profile. Desktop settings are missing and personal files are unavailable.

## Impact
User unable to access personal files or customised desktop settings.

## Environment
- Domain-joined Windows client
- User account: Domain standard user

## Investigation
- Logged in as domain administrator
- Observed temporary profile behaviour on login
- Checked Event Viewer → Windows Logs → Application
- Filtered by User Profile Service

## Findings
- Event ID 1511: Windows cannot find the local profile
- User profile folder previously renamed, causing registry mismatch

## Root Cause
Corrupted user profile reference in registry under ProfileList, causing Windows to load a temporary profile.

## Resolution
- Opened Registry Editor
- Navigated to:
  HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
- Identified SID linked to affected user via ProfileImagePath
- Deleted corrupted SID entry
- Logged user out and back in to recreate clean profile
- Restored user files from old profile directory

## Verification
User logged in normally with no temporary profile warning. Desktop and files restored successfully.

## Tools Used
- Event Viewer
- Registry Editor
- File Explorer

## Status
Resolved
## Screenshots / Evidence
- [User-folder-renamed](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/72ac90e6e76b40d6fcaa60e9530f58d3b84bcf59/evidence/ticket-1/1-users-folder-renamed.png)
- [temp-profile-warning](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/65183a9426e50c116e56590f8b87aaf3772cf36e/tickets/Ticket-1-corrupted-user-profile.md)
- [filtering-logs](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/65183a9426e50c116e56590f8b87aaf3772cf36e/evidence/ticket-1/3-filtering-logs.png)
- [event-1511](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/a4d1e55064d4017e1f4a1711adc72ca02e660efe/evidence/ticket-1/4-event-1511.png)
- [registry-profilelist-sid](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/a4d1e55064d4017e1f4a1711adc72ca02e660efe/evidence/ticket-1/5_registry-profilelist-sid.png.png)
- [normal-login](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/a4d1e55064d4017e1f4a1711adc72ca02e660efe/evidence/ticket-1/6-normal-login.png)
