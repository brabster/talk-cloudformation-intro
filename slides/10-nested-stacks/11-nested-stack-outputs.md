## Nested Stacks

How to reference something in a nested stack?

Step 1: Define the value as an output

```yaml
Resources:
  EventStream: ...

Outputs:
  EventStreamArn:
    Description: Kinesis stream of events
    Value: !GetAtt EventStream.Arn
```

Note:

