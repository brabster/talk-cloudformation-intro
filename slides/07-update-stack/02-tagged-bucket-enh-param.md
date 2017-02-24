## Parameters, Refs, and Stack Updates

Parameters may be constrained, helping to catch invalid data earlier.

```yaml
Parameters:
  Purpose:
    Type: String
    Description: What is this stack for? <----- describe it!
    Default: MakingMoney <-------------- set a default value
    AllowedValues: <--------------- constrain allowed values
      - MakingMoney
      - Demo

Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      Tags:
        - Key: StackPurpose
          Value: !Ref Purpose
```

Note:
Parameter constraints will alter the behaviour of the CloudFormation console.

Values provided for a parameter must satisfy all constraints or the stack create/update will abort.

The Default parameter property will be taken if the parameter is not explicitly set.
