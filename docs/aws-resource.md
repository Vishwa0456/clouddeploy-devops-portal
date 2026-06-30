# CloudDeploy — AWS Resources

| Resource              | Count | Purpose                              |
|-----------------------|-------|--------------------------------------|
| EC2 Instance          | 1     | Hosts portal (Node.js + Nginx)       |
| Auto Scaling Group    | 1     | Scales EC2 under load                |
| Application Load Balancer | 1 | Routes traffic to EC2               |
| Aurora MySQL          | 1     | Stores users, projects, deployments  |
| S3 Bucket             | 1     | Stores uploaded ZIP files            |
| DynamoDB Tables       | 2     | DeploymentStatus, LiveLogs           |
| Lambda Functions      | 4-5   | Deployment automation                |
| Elastic Beanstalk     | 1     | Runs the deployed apps               |
| EFS                   | 1     | Shared logs across EC2               |
| EBS                   | 1     | Attached storage for EC2             |
| VPC                   | 1     | Network for everything               |
| Subnets               | 4     | 2 public, 2 private                  |
| Internet Gateway      | 1     | Public internet access               |
| NAT Gateway           | 1     | Private subnet internet access       |
| Security Groups       | 4     | ALB, EC2, RDS, EFS                   |
| IAM Roles             | 2     | EC2 role, Lambda role                |
| SNS Topic             | 1     | Email and SMS notifications          |
| CloudWatch Alarms     | 4     | CPU, storage, Lambda errors, health  |
