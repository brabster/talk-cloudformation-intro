## Cross-References

Refer to other resources

```yaml
Resources:
  MyS3Bucket: <------------------------ logical name of S3 bucket
    Type: AWS::S3::Bucket

  MyLogGroup:
    Type: AWS::Logs::LogGroup
    Properties:
     LogGroupName: !Ref MyS3Bucket <--- name log group for S3 bucket

```

Note:
* What is actually passed in a reference to a resource varies, check documentation
