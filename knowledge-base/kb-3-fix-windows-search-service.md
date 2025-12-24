# Fix Windows Search Not Working

## Symptoms
- Search indexing warning
- Slow or no search results

## Cause
Windows Search service disabled.

## Fix
1. Open services.msc
2. Set Windows Search to Automatic (Delayed Start)
3. Start service

## Verification
Search returns results instantly.

## Related Tickets
- TICKET-003

