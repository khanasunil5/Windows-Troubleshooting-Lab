# TICKET-002: Connected to Network but Cannot Access Internal Resources

## User-Reported Issue
User reports network shows as connected but cannot access internal company resources.

## Impact
User unable to access shared folders or domain services.

## Environment
- Windows domain client
- Host-only internal lab network
- Domain Controller providing DNS

## Investigation
- Verified physical/network connection
- Tested connectivity:
  - ping <DC-IP> succeeded
  - ping <DC-hostname> failed
- Ran nslookup for domain name (failed)
- Ran ipconfig /all

## Findings
- Incorrect DNS server configured on client
- DNS not pointing to Domain Controller

## Root Cause
Client DNS misconfiguration prevented name resolution for domain resources.

## Resolution
- Updated IPv4 settings to use Domain Controller IP as DNS server
- Flushed and re-registered DNS:
  ipconfig /flushdns
  ipconfig /registerdns

## Verification
- ping <DC-hostname> successful
- nslookup resolved domain correctly
- Access to shared folders restored

## Tools Used
- Command Prompt
- Network Adapter Settings

## Status
Resolved

