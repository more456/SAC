# Backup, maintenance & recovery

## **BACKUP**

**Database Backup**

Aurora RDS cluster default backup is configured for 00:00-00:30

User can choose the Backup Retention policy

![](<../../../.gitbook/assets/image (11).png>)

**EC2 Compute Backup**

For EC2 backup it is recommended to do regular snapshot backups as described [here](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html)

## **MAINTENANCE**

**Database Maintenance**

Default Aurora RDS cluster maintenance window is set to sun:16:00-sun:17:30

**EC2 Maintenance**

Please refer to [this](https://aws.amazon.com/maintenance-help/) guide to setup EC2 Maintenance windows

## **RESTORE**

**Database Restore**

To restore Aurora backup refer this [link](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Managing.Backups.html)

**EC2 Compute Restore**

To restore EC2 backup from snapshot refer this [link](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-restoring-volume.html)
