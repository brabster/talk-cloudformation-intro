## Cross-Stack References

Export an output value from one stack

```yaml
Outputs:
  BucketName:
    Value: !Ref ImageBucket
    Export:
      Name: !Sub "${AWS::StackName}-BucketName"
```

Import it into another with `Fn::ImportValue`

```yaml
Parameters:
  ImageBucketStackName:...

Resources:
  MyResource:
    Thumbnailer
      "Fn::ImportValue":
        !Sub "${ImageBucketStackName}-BucketName"
```

Note:
- Can't use !Fn syntax for sequential calls, eg. !ImportValue !Sub won't work
- Avoid tying stack lifecycles together
- Maybe easier to reason about
- What defines your environment?

