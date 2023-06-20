# Object Encryption

S3 doesn’t offer encryption at a bucket level. Encryption occurs at an object level.
How data is stored on disk in an encrypted way - Encryption at Rest 
Client Side Encryption --> objects encrypted by the client before they leave 
Server Side Encryption --> Encrypted in transit using HTTPS, objects are not encrypted in S3 endpoint, then once it hits S3 storage, it encrypts it. 

## Server-Side Encryption (SSE)
SSE is now mandatory 
There are three types of server-side encryption that can be used with S3. These different options have different tradeoffs in regards to trust, overhead, cost, resource consumption, etc.

1. Server-Side Encryption With Customer-Provided Keys (SSE-C)
2. Server-Side Encryption with Amazon S3-Managed Keys (SSE-S3) --> default [AES-256]
3. Server-Side Encryption With KMS KEYS Stored in AWS Key Management Service (SSE-KMS)

1. customer responsible of keys, S3 manages encryption and decryption
2. S3 creates key, manages key, and rotates key + encryption + Decryption
3. KMS manages keys, S3 encrypts, decrypts (pro: role separation)

