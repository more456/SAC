# Encryption

Default deployment does not enable encryption on Aurora RDS.

It is recommended to enable encryption for security

Amazon Aurora can encrypt your Amazon Aurora DB clusters. Data that is encrypted at rest includes the underlying storage for DB clusters, its automated backups, read replicas, and snapshots.

Amazon Aurora encrypted DB clusters use the industry standard AES-256 encryption algorithm to encrypt your data on the server that hosts your Amazon Aurora DB clusters. After your data is encrypted, Amazon Aurora handles authentication of access and decryption of your data transparently with a minimal impact on performance. You don't need to modify your database client applications to use encryption.

Please refer this [link](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Overview.Encryption.html#Overview.Encryption.Enabling) to for Enabling encryption for an Amazon Aurora DB cluster&#x20;

**How to enable encryption?**

**Amazon Aurora** allows you to encrypt your databases using keys you manage through AWS Key Management Service (KMS).&#x20;

_**Encryption and decryption are handled seamlessly, so you don’t have to modify your applications to access your data.**_

**How to manage Amazon RDS Encryption Keys?**

You can manage keys used for Amazon RDS encrypted instances using the AWS Key Management Service (AWS KMS) in the IAM console.

**AWS KMS** is a service which enables you to create and use the encryption keys to protect your data.

**What is the cost for implementing Encryption at Rest?**

Encryption at rest is available at no additional cost in all Amazon regions. AWS KMS usage is billed at standard rates. There is no charge for the encryption; you will be charged for the calls that Aurora DB makes to AWS KMS.

**What are the limitations for implementing Encryption at Rest?**

You can only enable encryption for an Amazon RDS DB instance when you create it, not after the DB instance is created.

Step 1: Because you can encrypt a copy of an unencrypted snapshot, you can effectively add encryption to an unencrypted DB instance which was deployed by the Template.

Step 2: That is, you can create a snapshot of your DB instance, and then create an encrypted copy of that snapshot.&#x20;

Step 3: You can then restore a DB instance from the encrypted snapshot, and thus you have an encrypted copy of your original DB instance. For more information, see [Copying a snapshot](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER\_CopySnapshot.html).

Since you can encrypt a copy of an unencrypted snapshot, this way, you can quickly add encryption to a previously unencrypted DB instance. That is, you can create a snapshot of your DB instance when you are ready to encrypt it, and then create a copy of that snapshot and specify a AWS KMS CMK to encrypt that snapshot copy. You can then restore an encrypted DB instance from the encrypted snapshot.

You can refer this [link](https://aws.amazon.com/blogs/database/applying-best-practices-for-securing-sensitive-data-in-amazon-rds/) for best practices

During Cloud Formation deployment below VPC and Subnets are used - If you need to recreate the RDS database below should be used in the network configuration

![](<../../../.gitbook/assets/image (25).png>)

