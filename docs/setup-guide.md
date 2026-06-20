# Setup Guide

## Step 1: Launch EC2 Instance

Configuration:

* Ubuntu 22.04 LTS
* t3.micro
* 8 GB Storage

Security Group Rules:

* SSH (22)
* HTTP (80)

---

## Step 2: Connect to Instance

```bash
ssh -i key.pem ubuntu@PUBLIC_IP
```

## Step 3: Update System

```bash
sudo apt update
sudo apt upgrade -y
```

## Step 4: Install Docker

```bash
sudo apt install docker.io -y
```

Enable Docker:

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verify Installation:

```bash
docker --version
```

## Step 5: Install CloudWatch Agent

```bash
wget https://amazoncloudwatch-agent.s3.amazonaws.com/ubuntu/amd64/latest/amazon-cloudwatch-agent.deb

sudo dpkg -i amazon-cloudwatch-agent.deb
```

## Step 6: Configure CloudWatch Agent

Configure metrics collection for:

* Memory
* Disk
* Swap

## Step 7: Start CloudWatch Agent

```bash
sudo systemctl start amazon-cloudwatch-agent
```

Verify:

```bash
sudo systemctl status amazon-cloudwatch-agent
```

## Step 8: Create SNS Topic

Create SNS Topic:

MultiTierAppAlerts

Subscribe Email Address

Confirm Subscription

## Step 9: Create CloudWatch Alarms

Create:

* CPU Alarm
* Memory Alarm
* Disk Alarm

## Step 10: Create Dashboard

Add widgets for:

* CPU Utilization
* Memory Usage
* Disk Usage

Dashboard Name:

MultiTierAppDashboard
