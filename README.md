# kcns-aws-outposts-monitoring-dashboard
This repo contains AWS cloudformation code to deploy a sample AWS Outposts monitoring dashboard

# AWS Outposts CloudWatch Dashboard - CloudFormation Template

## Overview
This CloudFormation template automates the creation of an AWS CloudWatch Dashboard for monitoring AWS Outposts. The dashboard provides key metrics such as:
- **Connected Status** of the Outpost
- **Capacity Exceptions** for instance launches
- **Used and Available Instance Types**
- **Used and Available Reserved Instances**
- **Instance Type Capacity Utilization and Availability**
- **EBS Volume Type Capacity Utilization and Availability**
- **S3/Outposts Capacity Utilization and Availability**

## Prerequisites
Before deploying this CloudFormation template, ensure the following:
- You have appropriate IAM permissions to create CloudWatch Dashboards.
- You have an AWS Outpost ID.
- You know the AWS Region where your Outpost is located.

## Parameters
| Parameter | Description | Default |
|-----------|-------------|---------|
| `DashboardName` | Name of the CloudWatch Dashboard | `Outposts-Dashboard` |
| `OutpostId` | AWS Outpost ID | Required |
| `Region` | AWS Region where the Outpost is located | Required |
| `AccountId` | AWS Account ID | Required |

## Deployment Instructions
Follow these steps to deploy the CloudFormation stack:
1. Open the [AWS CloudFormation Console](https://console.aws.amazon.com/cloudformation/) in the region where the Outposts device is connected.
2. Click on **Create Stack** > **With new resources (standard)**.
3. Upload the `outposts-dashboard.yml` file or copy-paste the template into the editor.
4. Enter the required parameters.
5. Click **Next** and configure stack options as needed.
6. Click **Create Stack** and wait for the deployment to complete.
7. Navigate to **CloudWatch Dashboards** to view the newly created dashboard.

## Expected Dashboard Output
The created CloudWatch dashboard will include:
- **Widgets for Outpost status and capacity monitoring**
- **Instance and volume utilization metrics**
- **Graphical representation of resource availability**

## Sample Screenshots
Sample screenshots of CloudFormation execution and the created CloudWatch dashboard.
![image](https://github.com/Venkat7882/aws-outposts-monitoring-dashboard/images/image1.png)

![image](https://github.com/Venkat7882/aws-outposts-monitoring-dashboard/images/image2.png)


## Cleanup
To delete the CloudWatch Dashboard, delete the CloudFormation stack by following these steps:
1. Open the **AWS CloudFormation Console**.
2. Find the deployed stack in the **Stacks** list.
3. Click **Delete Stack** and confirm.

## License
This project is licensed under the [MIT License](LICENSE).

## Contributions
Feel free to contribute enhancements or report issues via GitHub Issues.


