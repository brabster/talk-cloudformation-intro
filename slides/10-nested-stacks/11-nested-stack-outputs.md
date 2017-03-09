## Nested Stacks

How to reference something in a nested stack?

Step 1: Define the value as an output

```yaml
Resources:
  ImageBucket: ...

Outputs:
  BucketName:
    Description: User upload image bucket
    Value: !Ref ImageBucket
```

Note:

