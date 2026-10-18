# SEIR Foundations — Lab 0: Your First EC2 Dashboard

## 1. Deployment Evidence

| Deployment | Public IPv4 Address | Connection Method | Screenshot | Terminated? |
|---|---|---|---|---|
| 1 | 52.11.2.190 | SSH via Git Bash | `Screenshots/seir52.11-2.png`| Yes |
| 2 | 35.90.51.199 | SSH via Git Bash | `Screenshots/35.90-3.png` | Yes |
| 3 | 35.88.76.206 | SSH via Git Bash | `Screenshots/35.88.76.20-2.png` | Yes |

## 2. What I Did

For each deployment, I launched an EC2 instance using my saved launch template in AWS Oregon (`us-west-2`). I recorded the public IPv4 address, connected using SSH through Git Bash, ran `seir-dashboard`, captured a screenshot, and terminated the instance after collecting evidence.

## 3. Understanding the Dashboard

- **CPU:** Shows how much processing power the instance is using.
- **Memory:** Shows how much RAM is in use.
- **Disk:** Shows how much storage is being used.
- **Uptime:** Shows how long the system has been running since it started.

## 4. What Became Easier

Repeating the deployment process made it easier to launch instances from my template, find public IP addresses, connect through SSH, and display the dashboard.

## 5. Errors and Troubleshooting

I initially had SSH connection difficulties. I resolved them by using Git Bash and specifying my SSH private key when connecting.

## 6. Cleanup

I terminated all three practice instances after collecting evidence. I retained my launch template and checked for leftover EBS volumes and Elastic IP addresses.

