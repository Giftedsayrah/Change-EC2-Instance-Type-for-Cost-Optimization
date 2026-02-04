# Change-EC2-Instance-Type-for-Cost-Optimization

This guide documents how to change an AWS EC2 instance type from **t2.micro** to **t2.nano** to optimize resource utilization and cost.  
The task ensures that all **status checks are completed** before making changes and that the instance is **running successfully** afterward.

## Step 1: Log in to the AWS Management Console

Sign in to the AWS Management Console using your credentials.

![AWS Console Login](images/01-aws-console-login.png)

## Step 2: Navigate to the EC2 Dashboard
- From the AWS services menu, select **EC2**
- Click **Instances** from the left navigation pane
![EC2 Dashboard](images/02-ec2-dashboard.png)

## Step 3: Locate the EC2 Instance
- Search for the instance named **xfusion-ec2**
- Select the instance checkbox
![Locate EC2 Instance](images/03-locate-instance.png)

## Step 4: Verify Instance Status Checks
Before making any changes, confirm that the instance has completed its status checks.
- Ensure **Status check = 2/2 checks passed**
- If the status shows **Initializing**, wait until checks are complete

## Step 5: Stop the EC2 Instance
Changing an instance type requires the instance to be stopped.
- Select the instance
- Click **Instance state**
- Choose **Stop instance**
- Confirm the action
![Stop Instance](images/05-stop-instance.png)
Wait until the **Instance state** changes to **Stopped**.

## Step 6: Change the Instance Type
- Select the stopped instance
- Click **Actions**
- Navigate to **Instance settings**
- Click **Change instance type**
![Change Instance Type Menu](images/06-change-instance-type.png)

- Select **t2.nano**
- Click **Apply**
![Select t2.nano](images/07-select-instance-type.png)

## Step 7: Start the EC2 Instance
- Select the instance
- Click **Instance state**
- Choose **Start instance**
![Start Instance](images/08-start-instance.png)

## Step 8: Final Verification
Confirm the following:
- Instance name: **xfusion-ec2**
- Instance type: **t2.nano**
- Instance state: **Running**
- Status checks: **2/2 checks passed**

![Final Verification](images/09-final-verification.png)

## Conclusion

- Changing the EC2 instance type is an effective way to optimize cost for underutilized resources.
- Always ensure status checks are completed before making configuration changes.
- Downsizing instances like this supports AWS cost optimization best practices and efficient cloud resource management.
 
