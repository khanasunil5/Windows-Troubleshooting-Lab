# Shared Folder Access Denied

## User-Reported Issue
User receives "Access is denied" when accessing shared folder.

## Impact
User unable to access departmental files.

## Environment
- Windows Server file share
- Domain user accessing \\Server\Finance

## Investigation
- Verified network connectivity
- Checked share permissions
- Checked NTFS permissions
- Used Effective Access to validate permissions

## Findings
- User missing NTFS permissions
- Share permissions alone insufficient

## Root Cause
Incorrect NTFS permissions blocking access despite share availability.

## Resolution
- Added user group to NTFS permissions
- Applied Modify access following least-privilege principle

## Verification
User accessed shared folder successfully and created test file.

## Tools Used
- File Explorer
- NTFS Security tab
- Effective Access

## Status
Resolved

