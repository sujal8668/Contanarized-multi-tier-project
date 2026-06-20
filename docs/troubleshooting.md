# Troubleshooting Guide

## Issue: CloudWatch Agent Not Running

Check Status:

```bash
sudo systemctl status amazon-cloudwatch-agent
```

Restart:

```bash
sudo systemctl restart amazon-cloudwatch-agent
```

---

## Issue: Memory Metric Missing

Verify Agent Configuration:

```bash
sudo cat /opt/aws/amazon-cloudwatch-agent/etc/amazon-cloudwatch-agent.d/file_file_config.json
```

Restart Agent:

```bash
sudo systemctl restart amazon-cloudwatch-agent
```

Wait 5 minutes.

---

## Issue: Disk Metric Missing

Verify:

disk_used_percent

exists in configuration.

Restart agent after changes.

---

## Issue: SNS Email Not Received

Verify:

* Email subscription confirmed
* Alarm action enabled
* SNS Topic attached to alarm

---

## Issue: Alarm Always In Alarm State

Check threshold values.

Incorrect:

Threshold > 1

Correct:

Threshold > 80

Update and save alarm.

---

## Issue: Docker Service Not Running

Check:

```bash
sudo systemctl status docker
```

Start:

```bash
sudo systemctl start docker
```

---

## Issue: EC2 Website Not Accessible

Verify:

* Instance running
* HTTP Port 80 allowed
* Web service running

Check Security Group:

Inbound Rule:

HTTP (80) → 0.0.0.0/0
