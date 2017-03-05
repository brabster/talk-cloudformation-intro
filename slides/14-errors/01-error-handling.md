## Error Handling

CloudFormation will attempt to roll back changes on error

`Rollback Failed` state could occur if:
- resource were changed outside of CloudFormation
- IAM permissions prevent the rollback action
- Limits prevent rollback
- and many other reasons

Note:
- See AWS documentation or AWS support if you see this
