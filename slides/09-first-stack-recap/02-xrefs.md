## Cross-References

Refer to parameters, as in tagged bucket example

```yaml
Parameters:
  Purpose: <----------------------- parameter logical name
    Type: String

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      Tags:
        - Key: StackPurpose
          Value: !Ref Purpose <---- cross-reference

```

Note:
* Keys in the template map referred to as "logical names"
* *!Ref* takes an argument of the resource to substitute
