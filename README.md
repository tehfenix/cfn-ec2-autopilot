# cfn-ec2-autopilot
These are my personal autopilot scripts for demonstration purposes only.

### CFN-demo-Lambda-nonprod-autopilot.yaml
This stack deploys the following resources:
* IAM Role
* Lambda Function for starting instances
* Lambda Function for stopping instances
* Event for starting instances
* Event for stopping instances
* Lambda invocation permissions

This will automatically start / stop instances at the times determined in the CRON expressions for any EC2 instances with the following tag applies:

```
stage="non-prod"
```

#### TODO
1. Add parameters to allow custom CRON expressions to be used.
2. Add *autostart* tag so only relevant non-prod instances start automatically