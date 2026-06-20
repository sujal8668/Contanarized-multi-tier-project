# Testing Procedures

## CPU Alarm Test

Generate CPU Load:

```bash
sudo apt install stress -y

stress --cpu 2 --timeout 300
```

Expected Result:

* CPU Utilization increases
* Alarm triggers
* SNS Email received

---

## Memory Monitoring Test

Verify metric:

CloudWatch → Metrics → CWAgent

Metric:

mem_used_percent

Expected Result:

Metric available and updating.

---

## Disk Monitoring Test

Verify metric:

CloudWatch → Metrics → CWAgent

Metric:

disk_used_percent

Expected Result:

Metric available and updating.

---

## Dashboard Test

Open Dashboard:

MultiTierAppDashboard

Verify:

* CPU Widget
* Memory Widget
* Disk Widget

All displaying live data.

---

## SNS Notification Test

Trigger any alarm.

Expected Result:

Email notification received from Amazon SNS.

---

## Alarm Recovery Test

Stop stress workload.

Expected Result:

Alarm returns to OK state.
