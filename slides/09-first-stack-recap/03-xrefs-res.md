## Cross-References

Refer to other resources

```yaml
Resources:
  MyS3Bucket: <------------------------ logical name
    Type: AWS::S3::Bucket

  MyLogGroup:
    Type: AWS::Logs::LogGroup
    Properties:
     LogGroupName: !Ref MyS3Bucket <--- provisioned bucket name

```

Note:
* What is actually passed in a reference to a resource varies, check documentation
