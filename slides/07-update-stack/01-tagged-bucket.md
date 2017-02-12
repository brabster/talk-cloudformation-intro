## Parameters, Refs, and Stack Updates

Let's tag the bucket with a purpose. We'll use a parameter to specify the value.

```yaml
Parameters:
  Purpose:
    Type: String

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      Tags:
        - Key: StackPurpose
          Value: !Ref Purpose

```

Note:
From here, AWSTemplateFormatVersion and Description are omitted for presentation but set in the actual template.

The Parameters block specifies a "Purpose" parameter. This must be specified at stack create or update time.

The Resources block specifies a "Tags" property, assiging the value of the parameter to the tag "StackPurpose".
