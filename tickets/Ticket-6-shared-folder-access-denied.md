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

## Screenshots / Evidence
- [shares-permissions](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/1-shares-permissions.png)
- [finance-share-permissionsoad](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/2-finance-share-permissions.png)
- [finance-ntfs-permissions](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/3-finance-ntfs-permissions.png)
- [user-access-finance](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/4-user-access-finance.png)
- [permissions-removed](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/5-permissions-removed.png)
- [access-denied](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/6-access-denied.png)
- [share-permissions-check](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/7-share-permissions-check.png)
- [ntfs-permissions-check](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/8-ntfs-permissions-check.png)
- [effective-access](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/9-effective-access.png)
- [permissions-restored](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/10-permissions-restored.png)
- [access-restored](https://github.com/khanasunil5/Windows-Troubleshooting-Lab/blob/fbee359db20ad46c3532bb0cd53b048b3a80f0cc/evidence/ticket-6/11-access-restored.png)

