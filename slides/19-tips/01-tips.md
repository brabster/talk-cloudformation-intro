## General Tips

- Introduce CloudFormation as early as possible
- Don't update CloudFormation-managed resources yourself
- Have at least one test environment and test EVERYTHING
- Integrate your infra code with your CI/CD pipeline
- Keep infra code with the code it provisions
- Organise your templates to group things that change together
- Use multiple AWS accounts, one per "environment"

Note:
- It's easier to get started with IaC and CloudFormation while you have less stuff to manage
- Many CF-managed resource properties can be safely updated, eg. DynamoDB capacity, and it's a quick way to spike something out
- But be disciplined, use your pipelines, don't let your config drift. Good practice is to let CF do the updates.
- The infrastructure code will be coupled to what it provisions. Keep them together, because they will change together.
- A corollary which is probably obvious - your templates are code, keep them in version control!
- An AWS account is the only real partitioning of AWS infrastructure, both for resources and for considerations like billing and limits. They don't cost anything, and with CloudFormation you can maintain equivalent infra across accounts.
