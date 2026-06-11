# 3-Tier-Serverless-RSVP-App-Deployment-Using-CloudFormation
Automated 3-tier AWS deployment using CloudFormation: S3/CloudFront (Web), API Gateway/Lambda (App), and RDS/DynamoDB (Database).

<img width="1408" height="768" alt="image_f53b9a" src="https://github.com/user-attachments/assets/c1a609aa-a815-4bce-903e-415d7303efe2" />

This template file provisions this infrastructure by;
1. Creates a custom VPC
2. Creates three subnets
3. Creates a route table
4. Associates the route table with the three subnets
5. Create an internet gateway and associates it with the route table making all the subnets public
6. Creates a security group with two rules. First one to allow all traffic from our development PC to the RDS and second rule to allow resources in this security group to access the RDS on port 3306
7. Creates a DB subnet group and associate subnets with it.
8. Provision an RDS MySQL instance (db.t3.micro) in our defined custom VPC and the DB Subnet group. Turn on Publicly accessible.
