#### Using this Operational Lambda
This Lambda function integrates with [**Bottle Monitoring Lambda**](https://gitlab.com/bottle-tech/bottle-library/resource-monitoring-lambda) to monitor **Invocations** and **Throttles**
You have to supply the values for the following parameters
- **invocation_threshold** - Number of times Lambda function is invoked in 1 minute, default is 30 times, if crossed activates the alarm
- **throttled_count** - No. of times Lambda function was throttled, default is 5 times
- **Profile**

To deploy this Lambda function use the following behaviour :
```
sls deploy --invocation_threshold 30 --profile learn --throttled_count 5
```
In **Alarm Actions** there is a SNS topic **SNSTopicMonitorBottleLambda** which was imported from another Stack.
