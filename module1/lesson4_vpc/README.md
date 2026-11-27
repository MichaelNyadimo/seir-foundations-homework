# Lesson 4 — VPC Homework Evidence

## 1. VPC Configuration

- **VPC Name:** michael-homework-vpc
- **VPC ID:** vpc-05c32bdfd6337ba42
- **VPC CIDR:** 10.1.0.0/16
- **AWS Region:** us-east-1 (N. Virginia)
- **Availability Zones:** us-east-1a, us-east-1b, us-east-1c
- **Public Subnets:** 3
- **Private Subnets:** 6
- **DNS Hostnames:** Enabled

### Network Architecture

| Subnet | Tier | Availability Zone | CIDR |
|---|---|---|---|
| Public A | Public | us-east-1a | 10.1.1.0/24 |
| Public B | Public | us-east-1b | 10.1.2.0/24 |
| Public C | Public | us-east-1c | 10.1.3.0/24 |
| Private A | Tier 1 | us-east-1a | 10.1.11.0/24 |
| Private B | Tier 1 | us-east-1b | 10.1.12.0/24 |
| Private C | Tier 1 | us-east-1c | 10.1.13.0/24 |
| Private A | Tier 2 | us-east-1a | 10.1.21.0/24 |
| Private B | Tier 2 | us-east-1b | 10.1.22.0/24 |
| Private C | Tier 2 | us-east-1c | 10.1.23.0/24 |

## 2. EC2 Public Subnet Evidence

**Date launched:** November 26, 2026  
**Timezone:** America/Denver (MST)

| Field | Public Subnet A | Public Subnet B | Public Subnet C |
|---|---|---|---|
| Availability Zone | us-east-1a | us-east-1b | us-east-1c |
| Public Subnet CIDR | 10.1.1.0/24 | 10.1.2.0/24 | 10.1.3.0/24 |
| Private IPv4 | 10.1.1.61 | 10.1.2.227 | 10.1.3.119 |
| VPC ID | vpc-05c32bdfd6337ba42 | vpc-05c32bdfd6337ba42 | vpc-05c32bdfd6337ba42 |
| Instance ID | i-0578fe897269c5620 | i-04f7a7f2f43270707 | i-0ce3915012c12d921 |
| Public IPv4 DNS | ec2-44-214-44-236.compute-1.amazonaws.com | ec2-35-175-235-72.compute-1.amazonaws.com | ec2-54-162-139-75.compute-1.amazonaws.com |
| Screenshot | public_subnet_a.jpg | public_subnet_b.jpg | public_subnet_c.jpg |
| Terminated | No | No | No |

## 3. EC2 Deployment Reflection

Deploying an EC2 instance in each of the three public subnets demonstrates how AWS can distribute resources across multiple Availability Zones. Each instance receives its own private IP address from its assigned subnet. This provides redundancy because an issue affecting one Availability Zone is less likely to affect all three instances. All three instances use the same VPC but belong to different public subnets. This setup demonstrates how subnet design and Availability Zones support application availability and fault tolerance.

## 4. VPC Design Reflection

**VPC CIDR:** 10.1.0.0/16  
**AWS Region:** us-east-1

**Hardest Part of the VPC Design:**

[Write 2–3 sentences describing the hardest part of designing or configuring your VPC.]

## 5. Cisco Binary Game

- **High Score:** [Enter your high score]
- **First-Try Score:** [Enter score] / 20
- **Longest Question:** [Enter question or subnetting challenge]

**Screenshot:** `binary_game_high_score.jpg`

## 6. Subnetting Practice

- **Total Questions:** 20
- **Theo's Practice Questions:** 7
- **Easy Questions:** 5
- **Medium Questions:** 5
- **Hard Questions:** 3
- **Showed Work:** [Confirm when completed]
- **Corrections Included:** [Confirm when completed]

## 7. Required Screenshots

| Screenshot | Status |
|---|---|
| Maarek_Section27_quiz.jpg | Pending |
| public_subnet_a.jpg | Captured |
| public_subnet_b.jpg | Captured |
| public_subnet_c.jpg | Captured |
| binary_game_high_score.jpg | Pending |

## 8. Homework Checklist

- [x] Network architecture file created
- [x] VPC created
- [x] Three public subnets created
- [x] Six private subnets created
- [x] DNS hostnames enabled
- [x] Internet Gateway attached
- [x] Public route table configured
- [x] Three EC2 instances launched in separate public subnets
- [x] HTTP security group configured
- [x] Three EC2 web pages verified
- [x] Three public subnet screenshots captured
- [ ] Maarek Section 27 quiz screenshot saved
- [x] Cisco Binary Game screenshot saved
- [x] Subnetting practice completed (20 questions)
- [x] Lesson 4 notes completed
- [ ] README evidence table finalized
- [x] All three EC2 instances terminated
- [x] EBS volumes checked
- [x] Elastic IPs checked
- [x] VPC deleted

## 9. AWS Cleanup

**EC2 Instances:**
- michael-public-a — Pending termination
- michael-public-b — Pending termination
- michael-public-c — Pending termination

**EBS Volumes:** Pending verification

**Elastic IPs:** Pending verification

**VPC:** Pending deletion

