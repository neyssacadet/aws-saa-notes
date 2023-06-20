# S3 Lifecycle Configuration 
Set of rules applied to the bucket. Rules consist of actions applied to a bucker or groups of objects. 
Types of actions: 
- transition actions
- expiration actions

## Transitions
- ![image](https://github.com/neyssacadet/aws-saa-notes/assets/51377285/0be5533d-35e7-4dd6-893f-4c1d8cb30110)


# S3 Replication 
S3 has two replication features that allow objects to be replicated between SOURCE and DESTINATION buckets in the same or different AWS accounts. Replication is encrypted 

- Cross-Region Replication (CRR) is the process used when Source and Destination are in different AWS regions
- Same-Region Replication (SRR) is used when the buckets are in the same region.

## S3 Replication Options
All objects or a subset of objects can be replicated.
Which Storage class to use (Default is to maintain, can be overriden)
Ownership - default is the source account
RTC Replication Time Control. guaranteed level of predictability, and it monitors. (15 minutes of replication)

## Powerup
Replication is not retroactive by default.
Versioning needs to enabled 
Batch Replication --> used to replicated existing objects 
One way replication (source to destination) 
Unencrypted 
Source bucket owner nedds permissions to objects 
No system events, Glacier or Glacier Deep Archive (Cannot be replicated) 
No deletes are replicated. Can enable it though 

## Why use replication? Use Cases 
- Log Aggregation
- PROD and TEST Synchronization
- Resilience with strict sovereignty
- Latency reduction
  

