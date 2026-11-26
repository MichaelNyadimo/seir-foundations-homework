
# Lesson 4 — VPC Notes

## Why Deploy EC2 Instances Across Three Public Subnets?

Deploying EC2 instances across three different public subnets allows them to operate in separate Availability Zones. This improves availability because an issue affecting one Availability Zone is less likely to affect all three instances. Each instance receives its own private IP address within its assigned subnet. Distributing instances across multiple Availability Zones also provides redundancy and supports fault tolerance. This architecture demonstrates how AWS networking can help keep applications available if one Availability Zone experiences a disruption.
