Lesson 2 — Slack Alerts Homework Notes

HW1 — Hello Slack

The alert successfully reached the #balerica-alerts Slack channel. This confirmed that my EC2 instance could send a custom notification through the Slack integration.

HW2 — Severity Tour

During the original run, CRITICAL, ERROR, and WARNING alerts arrived because the configured threshold was INFO. The INFO threshold allows alerts at INFO severity and above.

Experiment 1 — Prediction vs. Result

Prediction: Only CRITICAL alerts would reach Slack when the threshold was changed to CRITICAL.

Result: Only the CRITICAL alert arrived. ERROR and WARNING were filtered out.

Conclusion: The severity threshold controls which alerts are delivered.

HW3 — Server Time

The server reported 06:16 UTC. Denver was on Mountain Daylight Time (UTC-6) at that time.

The difference was 6 hours. Servers commonly use UTC to maintain consistent timestamps across different locations.

HW4 — Disk Watch

A quiet INFO alert is good design because it prevents unnecessary notifications for routine events. This reduces alert fatigue and makes important warnings and critical incidents easier to notice.

Experiment 3: Disk usage was 25.3%. After lowering the WARNING threshold to 20%, the script classified disk usage as WARNING. The alert was skipped by the configured severity threshold.

HW5 — Load Check

The load average could spike if the Balerica bank experiences heavy transaction processing, many simultaneous requests, CPU-intensive tasks, or multiple batch jobs running at once.

HW6 — Incident Drill

A payment rejection rate above 5% deserves immediate human attention because customers may be unable to complete payments.

A batch job running 12 minutes longer than usual should also be investigated, particularly if it threatens an important processing deadline.

HW7 — Morning Report

The morning report successfully collected the server's time, hostname, Python version, disk usage, and system load. It provides a quick overview of server health.

Experiment 2 — Kill Switch

I set SLACK_ALERTS_ENABLED=false and tested the send_alert function directly. No message appeared in Slack.

This demonstrated that the kill switch can suppress alert delivery without removing the alert-sending functionality.

Final Configuration Restoration

Restored the configuration to:

SLACK_ALERT_SEVERITY=INFO

SLACK_ALERTS_ENABLED=true
