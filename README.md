# CloudWatch-Alarms-AWS

The new CloudWatch Alarms feature allows you to watch CloudWatch metrics and to receive notifications when the metrics fall outside of the levels.

Steps to create an alarm for EC2 CPU utilisation-

```

To create an alarm based on CPU usage

1 Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

2. In the navigation pane, choose Alarms, Create Alarm.

3. Choose Select metric.

4. In the All metrics tab, choose EC2 metrics.

5. Choose a metric category (for example, Per-Instance Metrics).

6. Find the row with the instance that you want listed in the InstanceId column and CPUUtilization in the Metric Name column. Select the check box next to this row, and choose Select metric.

7. Under Specify metric and conditions, for Statistic choose Average, choose one of the predefined percentiles, or specify a custom percentile (for example, p95.45).

8. Choose a period (for example, 5 minutes).

9. Under Conditions, specify the required data:

10. For Threshold type, choose Static.

11. Choose Next.

12. Under Notification, choose In alarm and select an SNS topic to notify when the alarm is in ALARM state

13. To have the alarm send multiple notifications for the same alarm state or for different alarm states, choose Add notification.

14. To have the alarm not send notifications, choose Remove.

15. When finished, choose Next.

16. Enter a name and description for the alarm. The name must contain only ASCII characters. Then choose Next.

17. Under Preview and create, confirm that the information and conditions are what you want, then choose Create alarm.

```
