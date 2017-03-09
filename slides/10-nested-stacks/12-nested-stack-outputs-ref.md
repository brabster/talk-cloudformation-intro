## Nested Stacks

How to reference something in a nested stack?

Step 2: Ref the value from the parent template

```yaml
Resources:
  ImageBucketStack: ...

  Thumbnailer:
    Type: ...
    Properties:
      BucketName: !GetAtt ImageBucketStack.Outputs.BucketName
```

Note:

