AWS Cloud Cost Optimization - Identifying Stale Resources
Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.
Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.


![image](https://github.com/Shreyashbhise/aws-cost-optimization-project/assets/108046802/a5013d1b-996e-4c6c-a099-740289afcaff)

