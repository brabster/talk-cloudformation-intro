## Custom Resources

Example:

```yaml
AppHealthcheck:
  Type: Custom::PingdomPing
  Properties:
    ServiceToken: !GetAtt PingdomPingCustomResource.Arn
    PingTargetUrl: !GetAtt AppUrl
```

Note:
- Type may be "AWS::CloudFormation::CustomResource" or "Custom::WhateverYouWant"
- "Custom::WhateverYouWant" is a lot better in cli/sdk/console output!
- ServiceToken must be the ARN of an AWS Lambda function to process the CloudFormation messages
- Other Properties are passed to the implementing function as parameters
