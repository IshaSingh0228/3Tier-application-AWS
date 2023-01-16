# 3Tier-application-AWS
Steps to create 3tier application using aws services using VPC, EC2, LB, RDS

A 3-Tier Architecture is made up of 3 separate tiers: the Presentation Layer, or Web Tier, The Application Tier, and Database Tier.

**Web Tier**
1. 2 public subnets
2. Create 1 EC2 instances in any 2AZ
3. EC2 Web Server Security Group allowing inbound permission from the internet.
4. Boot strap static web page
5. Create a public route table and associate the 2 public subnets.

**Application Tier**
1. 2 private subnets
2. Create 1 EC2 instances in any 2AZ
3. EC2 Application Server Security Group allowing inbound permission from the Web Server Security Group.
4. Associate with private route table. 
NOTE: Its just a demo, not implementing a actual application

**Database Tier**
1. Use a free Tier MySQL RDS Database.
2. The Database Security Group should allow inbound traffic for MySQL from the Application Server Security Group.
3. 2 private subnets.
4. Associate with private route table.



