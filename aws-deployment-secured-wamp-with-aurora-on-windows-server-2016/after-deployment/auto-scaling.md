# Auto-Scaling

During deployment Auto-Scaling for Aurora RDS is not configured

To enable Auto-Scaling you will need to add a replica. Please follow the below steps:

**Step1:** Add a replica

Navigate to the RDS cluster from Resources of the Cloud formation template&#x20;

![](<../../.gitbook/assets/image (16).png>)

Or go to [https://console.aws.amazon.com/rds](https://console.aws.amazon.com/rds)

![](<../../.gitbook/assets/image (1).png>)

Click on the database under RDS cluster -> Click on Instance Actions -> Create aurora replica

![](<../../.gitbook/assets/image (19).png>)

Give a name to the replica in the replica creation window. You will see the replica being created

![](<../../.gitbook/assets/image (20).png>)

Once the replica is created you can click on Actions on the RDS cluster and choose the option "Add replica to auto scaling"

![](<../../.gitbook/assets/image (3).png>)

**Step 2:** Aurora RDS can be configured using this [link](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/Aurora.Integrating.AutoScaling.html)

**To add an auto scaling policy to an Aurora DB cluster**

1. Sign in to the AWS Management Console and open the Amazon RDS console at [https://console.aws.amazon.com/rds/](https://console.aws.amazon.com/rds/).
2. In the navigation pane, choose **Databases**.
3. Choose the Aurora DB cluster that you want to add a policy for.
4. Choose the **Logs & events** tab.
5.  In the **Auto scaling policies** section, choose **Add**.

    The **Add Auto Scaling policy** dialog box appears.
6. For **Policy Name**, type the policy name.
7. For the target metric, choose one of the following:
   * **Average CPU utilization of Aurora Replicas** to create a policy based on the average CPU utilization.
   * **Average connections of Aurora Replicas** to create a policy based on the average number of connections to Aurora Replicas.
8.  For the target value, type one of the following:

    * If you chose **Average CPU utilization of Aurora Replicas** in the previous step, type the percentage of CPU utilization that you want to maintain on Aurora Replicas.
    * If you chose **Average connections of Aurora Replicas** in the previous step, type the number of connections that you want to maintain.

    Aurora Replicas are added or removed to keep the metric close to the specified value.
9. (Optional) Open **Additional Configuration** to create a scale-in or scale-out cooldown period.
10. For **Minimum capacity**, type the minimum number of Aurora Replicas that the Aurora Auto Scaling policy is required to maintain.
11. For **Maximum capacity**, type the maximum number of Aurora Replicas the Aurora Auto Scaling policy is required to maintain.
12. Choose **Add policy**.

The following dialog box creates an Auto Scaling policy based an average CPU utilization of 40 percent. The policy specifies a minimum of 5 Aurora Replicas and a maximum of 15 Aurora Replicas.![
&#x20;                   Creating an auto scaling policy based on average CPU
&#x20;                       utilization
&#x20;               ](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/images/aurora-autoscaling-cpu.png)

The following dialog box creates an auto scaling policy based an average number of connections of 100. The policy specifies a minimum of two Aurora Replicas and a maximum of eight Aurora Replicas.![
&#x20;                   Creating an Auto Scaling policy based on average&#x20;
&#x20;                       connections
&#x20;               ](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/images/aurora-autoscaling-connections.png)

When you click Add policy you have activated the Auto-Scaling

![](<../../.gitbook/assets/image (15).png>)

If you try to add Auto Scaling policy without adding at least one replica as detailed in Step 1 you will get a message like below

![](<../../.gitbook/assets/image (39).png>)



