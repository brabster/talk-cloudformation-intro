## Nested Stacks

How to reference something in a nested stack?

Step 2: Ref the value from the parent template

```yaml
Resources:
  EventStack: ...

  EventConsumer:
    Type: ...
    Properties:
      EventStreamArn: !GetAtt EventStack.Outputs.EventStreamArn
```

Note:

