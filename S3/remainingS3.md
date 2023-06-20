# S3 Select and Glacier Select 
S3 and Glacier Select allow you to use a SQL-Like statement to retrieve partial objects from S3 and Glacier.

S3 can store huge objects up to 5 TB
EX: CSV, JSON, Parquet etc 

# S3 Events
The Amazon S3 notification feature enables you to receive notifications when certain events happen in your bucket. To enable notifications, you must first add a notification configuration that identifies the events you want Amazon S3 to publish and the destinations where you want Amazon S3 to send the notifications. You store this configuration in the notification subresource that is associated with a bucket
Can be delivered to SNS, SQS, and lambda functions (resource policy needs to be provided). Types of notifications:
- Object created
- Object Delete
- Object Restore
- Replication

# S3 Access Logs
Server access logging provides detailed records for the requests that are made to a bucket. Server access logs are useful for many applications. For example, access log information can be useful in security and access audits. It can also help you learn about your customer base and understand your Amazon S3 bill.

# S3 Object Lock 
to store objects using a write-once-read-many (WORM) model. It can help you prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely. You can use S3 Object Lock to meet regulatory requirements that require WORM storage, or add an extra layer of protection against object changes and deletion.
Enabled on new buckets. For existing , need to contact AWS support. 
Requires versioning. 

Retention Period - specify days and years 
2 modes that can be applied when using retention period for S3 object lock: 
- compliance mode: cant be adjusted, deleted, overwritten (even by account root user). for compliance reasons, like medical and financial stuff
- governance: special permissions can be granted allowing settings to be adjusted 

Legal Hold - either ON or OFF
No retention 
No delete or changes until hold is removed 
Prevent accidental deletion of critical object versions 

# S3 Access Points 
a feature of S3, simplifies managing data access at scale for applications using shared data sets on S3. Access points are unique hostnames that customers create to enforce distinct permissions and network controls for any request made through the access point.
Simplifies managing access to S3 buckets/objects 
YOu can create many access points, each with different policies and different network access controls. Created via console or aws s3 control "create-access-point"
