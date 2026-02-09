### Data Requirements

| Area              | Title             | Description | Example(s) |
|-------------------|-------------------|-------------|------------|
| Data Requirements | Data Retention    | NFRs in this category are formed around topics such as: <br>• Data is to be retained in the active database partition for 120 days before archiving <br>• Durations for retention <br>• Data deleted from archive partition after 240 days <br>• Policies around what to archive and when | Data should be retained for 120 days then archived; deleted from archive after 240 days |
| Data Requirements | Data Transfer     | NFRs include: <br>• Transfer of files via SFTP <br>• Security around transfer method <br>• Files must be encrypted using AES‑256 <br>• Transfer must follow ISO 27001 <br>• Permitted transfer routes | Files transferred securely via SFTP using AES‑256 encryption following ISO 27001 |
| Data Requirements | Data Storage      | NFRs include: <br>• Active and Archive partitions must have encryption at rest <br>• Access to database must be role‑based, least privilege | Encrypted-at-rest DB partitions; role‑based access enforced |
| Data Requirements | Data Location     | NFRs include: <br>• All system data stored in the UK | UK‑only data storage |
| Data Requirements | Data Backup       | NFRs include: <br>• Full backup daily at 00:00 (< 90min) <br>• Incremental backups every 15/30/45 mins <br>• Backup to Master Copy <br>• Master Copy stored separately | Daily full backups; incremental every 15 min; Master Copy offsite |
| GDPR              | Ownership         | Topics include: Who owns the data, roles/responsibilities | Data owner defined per UK Gov guidance |
| GDPR              | Processing Consent | NFRs include: <br>• Personal data collected with explicit consent <br>• Anonymisation <br>• Breach notification within 24 hours | Consent required, data anonymised, UKHSA notified within 24h |