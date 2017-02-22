## Reusing our Bucket Stack

Our S3 stack can be nested without modification...

```yaml
Resources:
  FirstBucketStack:
    Type: AWS::CloudFormation::Stack
    Properties:
      TemplateURL: https://s3-eu-west-1.amazonaws.com/parameterless-bucket-stack-mys3bucket-5qd0jhtoo296/01-parameterless-s3-bucket.yaml

  SecondBucketStack:
    Type: AWS::CloudFormation::Stack
    Properties:
      TemplateURL: https://s3-eu-west-1.amazonaws.com/parameterless-bucket-stack-mys3bucket-5qd0jhtoo296/01-parameterless-s3-bucket.yaml
```
