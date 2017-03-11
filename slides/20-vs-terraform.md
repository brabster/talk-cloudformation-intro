## CloudFormation vs. Terraform

|      Feature      | CloudFormation | Terraform |
|:-----------------:|:--------------:|:---------:|
| Rollback on Error |        Y       |     n     |
|   Cross-Provider  |        n       |     Y     |
|   Execution Plan  |        ~       |     Y     |
|   Managed State   |        Y       |     n     |
|  IAM Integration  |        Y       |     n     |
|    Open Source    |        n       |     Y     |

Note:
- Terraform may get new AWS features before CloudFormation
- ...but may be better quality support when that feature hits CloudFormation?
- Cross-provider feature useful if you need it
- ...but different Terrform templates per-provider seems to be the norm, not quite as magic as it may appear
- ...and any use of provider-specific features would be problematic!
