# aws-secure-3tier-apps
AWS 3-Tier Web App Architecture with Security Controls and ISO 27001 Mapping 

# AWS Secure 3-Tier Application (Manual Console Project)
This hands-on project builds and secures a 3-tier web application architecture using the AWS Console.

It includes:
- Secure VPC network setup
- IAM least privilege roles
- Encrypted RDS database
- CloudTrail and Config logging
- Threat detection with GuardDuty
- WAF and S3 security
- ISO/IEC 27001:2022 control mapping

## Project Progress (Live Tracking)
- [x] VPC created
- [x] Subnets configured
- [x] Internet + NAT Gateway set up
- [ ] EC2 launched with IAM role
- [ ] RDS encrypted with KMS
- [ ] CloudTrail and Config enabled
- [ ] WAF + Security Hub configured
- [ ] ISO 27001 mapping drafted

##  Step 1: VPC + Subnet Setup

- Created custom VPC named `Secure3TierVPC`
- CIDR Block: `10.0.0.0/16`
- Created 3 subnets:
  - Public Subnet (for ALB): `10.0.1.0/24`
  - Private Subnet A (Web/App EC2): `10.0.2.0/24`
  - Private Subnet B (RDS): `10.0.3.0/24`
- Created Internet Gateway and attached it to the VPC
- Created NAT Gateway for private subnet internet access
- Updated Route Tables:
  - Public → IGW
  - Private → NAT GW

 **Screenshots:** (step by step)
 
| Step | Screenshot |
|------|------------|
| ✅ 1. VPC Created | ![](screenshots/vpc-created.png) |
| ✅ 2. Subnets Configured | ![](screenshots/subnet-list.png) |
| ✅ 3. Internet Gateway Attached | ![](screenshots/internet-gateway-config.png) |
| ✅ 4. NAT Gateway Created | ![](screenshots/nat-gateway-config.png) |
| ✅ 5. Public Route Table | ![](screenshots/route-table-public.png) |
| ✅ 6. Private Route Table | ![](screenshots/route-table-private.png) |

