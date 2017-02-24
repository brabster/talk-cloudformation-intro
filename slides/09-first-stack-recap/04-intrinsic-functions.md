## Intrinsic Functions

Compute values at deployment-time, like string joins

```yaml
Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket

  MyLogGroup:
    Type: AWS::Logs::LogGroup
    Properties:
     LogGroupName: !Join ["-", [!Ref MyS3Bucket, logs]]
```

See also <a href="http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference.html" target="_blank">Split, Sub, GetAtt, etc.</a>

Note:
* Why must the join be done at deployment-time?
* Functions that work with values that do not exist until the stack is being constructed.
