# CloudWatch Alarm Configuration

## CPU Alarm

Alarm Name: HighCPUAlarm

Metric:
CPUUtilization

Threshold:
Greater than 70%

Period:
1 Minute

Evaluation Periods:
1

Action:
SNS Email Notification

---

## Memory Alarm

Alarm Name: HighMemoryAlarm

Metric:
mem_used_percent

Threshold:
Greater than 80%

Period:
1 Minute

Evaluation Periods:
1

Action:
SNS Email Notification

---

## Disk Alarm

Alarm Name: HighDiskUsageAlarm

Metric:
disk_used_percent

Filesystem:
/

Threshold:
Greater than 80%

Period:
1 Minute

Evaluation Periods:
1

Action:
SNS Email Notification

---

## Notification Service

Amazon SNS

Notification Type:
Email

Purpose:
Send automated alerts whenever infrastructure thresholds are exceeded.

---

## Monitoring Metrics

* CPU Utilization
* Memory Utilization
* Disk Utilization
* CloudWatch Dashboard Visualization
* Email-Based Incident Alerting
