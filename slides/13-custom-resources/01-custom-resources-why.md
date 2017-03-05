## Custom Resources

Provision all the unsupported things!

for example...

- `Custom::SalesforceSandbox`
- `Custom::PingdomPing`
- `Custom::SlackNotifier`
- `Custom::BleedingEdgeAwsThing`
- `Custom::DatabaseMigration`

Note:
- Use custom resources to provision things that are not natively supported by CloudFormation eg.
  - SaaS like a Salesforce Sandbox
  - New AWS services tend to be supported by CloudFormation later, use custom resources to patch the gap
  - Your own custom infrastructure, like running database migrations during deployments
