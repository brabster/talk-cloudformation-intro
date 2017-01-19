## The Simplest Template?

This may be the simplest template that produces useful infrastructure!

```yaml
AWSTemplateFormatVersion: "2010-09-09"

Description: >
  Simplest CloudFormation Template - An S3 Bucket

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
```

Note:

Bucket name is not specified. Lets CloudFormation generate a suitable name.
Avoiding custom names is a good idea. We'll come back to that later.
