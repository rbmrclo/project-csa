# Amazon Glacier

- Amazon Glacier is an archival storage type
- Used for data that is NOT accessed frequently
- "Check out" and "check in jobs" can take several hours, meaning how long it
  can take for the data to be changed and/or retrieved
- Integrates with Amazon S3 lifecycle policies for easy archiving
- Very inexpensive and cost effective archival storage solution
- Glacier should NOT be used as a backup solution

NOTE: Glacier now offers three levels of data retrieval (pricing varies):

- Expedited: 1-5 minutes
- Standard: 3-5 hours
- Bulk: 5-10 hours
