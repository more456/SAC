# Instance Sizing

EC2 instance and Aurora components can be scaled up or down depending on the workload

Below EC2 instance sizes are offered:



Please refer to this [link](https://aws.amazon.com/ec2/instance-types/) for EC2 instance sizing

Default: t2.medium

Allowed:&#x20;

```
    "t2.micro",
    "t2.small",
    "t2.medium",
    "m3.medium",
    "m3.large",
    "m3.xlarge",
    "m3.2xlarge",
    "m4.large",
    "m4.xlarge",
    "m4.2xlarge",
    "m4.4xlarge",
    "m4.10xlarge",
    "c3.large",
    "c3.xlarge",
    "c3.2xlarge",
    "c3.4xlarge",
    "c3.8xlarge",
    "c4.large",
    "c4.xlarge",
    "c4.2xlarge",
    "c4.4xlarge",
    "c4.8xlarge",
    "g2.2xlarge",
    "hi1.4xlarge",
    "hs1.8xlarge",
    "i2.xlarge",
    "i2.2xlarge",
    "i2.4xlarge",
    "i2.8xlarge",
    "r3.large",
    "r3.xlarge",
    "r3.2xlarge",
    "r3.4xlarge",
    "r3.8xlarge"
```

Aurora component sizing information can be found at this [link](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Concepts.DBInstanceClass.html)

Below Aurora RDS Instance Type sizing are offered:&#x20;

Default: db.t2.medium

Allowed sizes: &#x20;

```
    "db.t2.medium",
    "db.r3.large",
    "db.r3.xlarge",
    "db.r3.2xlarge",
    "db.r3.4xlarge",
    "db.r3.8xlarge"
```

AWS Elastic LoadBalancer is automatically created where you can configure your DNS name.

