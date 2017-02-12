## Pseudo-Parameters

Values that provided by context, used with `!Ref`

```yaml
!Ref "AWS::Region"     <-- region stack is deployed in
!Ref "AWS::StackName"  <-- name of stack being deployed
```

...plus <a href="http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html" target="_blank">a few others</a>.

Note:
* Can be useful to construct ARNs or define default values
