#### Using this Operational Lambda
This Lambda function integrates with **Bottle Monitoring Lambda** to monitor **Invocations** and **Throttles**
You have to supply the values for the following parameters
**Invocations** - Number of times Lambda function is invoked in 1 minute, default is 30 times
**Throttles** - No. of times Lambda function was throttled, default is 5 times
**Profile**

To deploy this Lambda function use the following behaviour :
```sls deploy --invocation_threshold 30 --profile learn --throttled_count 5```