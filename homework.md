# SEIR Foundations — Lab 0: Your First EC2 Dashboard


## 1. Deployment Evidence

### Deployment 1

**Public IPv4:** `52.11.2.190`
![Deployment 1 Screenshot](Screenshots/seir52.11-2.png)



### Deployment 2

**Public IPv4:** `35.90.51.199`

![Deployment 2 Screenshot](Screenshots/35.90-2.png)


### Deployment 3

**Public IPv4:** `35.88.76.206`
![Deployment 3 Screenshot](Screenshots/35.88.76.20-2.png)

## 2. What I Did

For each of my deployments, I went and launched an EC2 instance 3 times using my saved launch template in AWS Oregon (`us-west-2`). I wrote down the public IPv4 addresses for all of them, connected using SSH method through Git Bash and ran `seir-dashboard` in Git Bash. After that, I captured my screenshots then finally terminated the instance once I was finished.

## 3. Understanding the Dashboard

- **CPU:** Displays how much processing power the instance is using.
- **Memory:** Displays how much RAM is in use.
- **Disk:** Displays how much storage is being used.
- **Uptime:** Displays how long the system has been running since starting.

## 4. What Became Easier

Repeating the deployment process made it easier to launch instances from my template, find public IP addresses, connect through SSH, and display the dashboard.

## 5. Troubleshooting and issues

I did have some SSH connection difficulties. I was able to solve them by using Git Bash and specifying my SSH private key when I tried to connect.

## 6. Cleanup

I terminated all three practice instances after capturing my information. I kept my launch template and checked for leftover EBS volumes that might be still lingering. 

