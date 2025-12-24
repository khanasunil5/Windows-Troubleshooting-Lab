Corrupted Windows User Profile (Temporary Profile Issue)

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
- Event ID 1509: Windows failed to load user profile
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

