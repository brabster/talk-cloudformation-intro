## Nested Stack Problems

- Opaque to:
  - CloudFormation Designer
  - CloudFormation Console
  - Change Sets
- Unstructured parameters could be limiting
- No libraries or dependency management for templates
- Can't be packaged with the code they need

Note:
- CloudFormation Designer can't "drill down" into Nested Stacks and doesn't reflect parameters and outputs
- CloudFormation UI doesn't treat Nested Stacks any differently to other stacks, no folding or dependency graphs, etc.
- Change Sets don't "drill down" into Nested Stacks, so all changes just look like "modify everything"
- Unstructured parameters - when I was thinking about a "message deduplicator" nested stack, I thought of a bunch of infrastructure with an AWS Lambda function that could be plugged in. The Lambda function would take different configuration depending on the usecase. Trying to create a nested stack meant that the structure of the Lambda's config had to be predetermined by the nested stack which was a problem for my case.

