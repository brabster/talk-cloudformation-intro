## Cross-Stack References

Export an output value from one stack

```yaml
Outputs:
  EventStreamArn:
    Value: !GetAtt EventStream.Arn
    Export:
      Name: !Sub "${AWS::StackName}-EventStreamArn"
```

Import it into another with `Fn::ImportValue`

```yaml
Resources:
  MyResource:...
    EventStreamArn:
      "Fn::ImportValue":
        !Sub "${EventStreamStackName}-EventStreamArn"
```

Note:
- Can't use !Fn syntax for sequential calls, eg. !ImportValue !Sub won't work
- Avoid tying stack lifecycles together
- Maybe easier to reason about
- What defines your environment?

