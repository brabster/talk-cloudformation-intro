## Reusing our Bucket Stack

Our S3 stack can be nested without modification...

```yaml
Resources:
  FirstBucketStack:
    Type: AWS::CloudFormation::Stack
    Properties:
      TemplateURL: https://s3.../01-parameterless-s3-bucket.yaml

  SecondBucketStack:
    Type: AWS::CloudFormation::Stack
    Properties:
      TemplateURL: https://s3.../01-parameterless-s3-bucket.yaml
```

Note:
- Template contains two nested stacks that use our prevously-defined template
