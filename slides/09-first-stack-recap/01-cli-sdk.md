## Alternatives to the Console

### AWS CLI <a href="http://docs.aws.amazon.com/cli/latest/reference/cloudformation/" target="_blank">(documentation)</a>

```bash
aws cloudformation create-stack --stack-name demo-stack --template-url ... --parameters ...
```

### AWS SDKs

<a href="https://aws.amazon.com/tools/" target="_blank">12 SDKs</a> at time of writing

### Integrations

Terraform <a href="https://www.terraform.io/docs/providers/aws/r/cloudformation_stack.html" target="_blank">resource</a>

Note:

* All CloudFormation functionality available through Console, CLI and SDKs
* Use CLI, SDKs to integration with other tooling
* Existing integrations into other ecosystems like Terraform
