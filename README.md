# CloudWatch-Alarms-AWS

The new CloudWatch Alarms feature allows you to watch CloudWatch metrics and to receive notifications when the metrics fall outside of the levels.

Steps to create an alarm for EC2 CPU utilisation-

```

To create an alarm based on CPU usage

Open the CloudWatch console at https://console.aws.amazon.com/cloudwatch/.

In the navigation pane, choose Alarms, Create Alarm.

Choose Select metric.

In the All metrics tab, choose EC2 metrics.

Choose a metric category (for example, Per-Instance Metrics).

Find the row with the instance that you want listed in the InstanceId column and CPUUtilization in the Metric Name column. Select the check box next to this row, and choose Select metric.

Under Specify metric and conditions, for Statistic choose Average, choose one of the predefined percentiles, or specify a custom percentile (for example, p95.45).

Choose a period (for example, 5 minutes).

Under Conditions, specify the following:

For Threshold type, choose Static.

For Whenever CPUUtilization is, specify Greater. Under than..., specify the threshold that is to trigger the alarm to go to ALARM state if the CPU utilization exceeds this percentage. For example, 70.

Choose Additional configuration. For Datapoints to alarm, specify how many evaluation periods (data points) must be in the ALARM state to trigger the alarm. If the two values here match, you create an alarm that goes to ALARM state if that many consecutive periods are breaching.

To create an M out of N alarm, specify a lower number for the first value than you specify for the second value. For more information, see Evaluating an alarm.

For Missing data treatment, choose how to have the alarm behave when some data points are missing. For more information, see Configuring how CloudWatch alarms treat missing data.

If the alarm uses a percentile as the monitored statistic, a Percentiles with low samples box appears. Use it to choose whether to evaluate or ignore cases with low sample rates. If you choose ignore (maintain alarm state), the current alarm state is always maintained when the sample size is too low. For more information, see Percentile-based CloudWatch alarms and low data samples.

Choose Next.

Under Notification, choose In alarm and select an SNS topic to notify when the alarm is in ALARM state

To have the alarm send multiple notifications for the same alarm state or for different alarm states, choose Add notification.

To have the alarm not send notifications, choose Remove.

When finished, choose Next.

Enter a name and description for the alarm. The name must contain only ASCII characters. Then choose Next.

Under Preview and create, confirm that the information and conditions are what you want, then choose Create alarm.

```
