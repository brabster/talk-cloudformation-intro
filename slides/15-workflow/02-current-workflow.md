## Our Current Workflow


- ~50 small "component" repos
- Original repo is still there
- CloudFormation everywhere

![Components compose into an environment template that is deployed to multiple environments on demand](images/cd-workflow/cd-workflow.dot.svg)

Note:
- Breaking down original repo is a work in progress
- Switched to CloudFormation because I'd used it before and I didn't fancy working with the shell scripts much!
- Turned out lots of stuff missing from the shell scripts
- Now running four "environments" across two AWS accounts, easy and pretty foolproof to spin up a new environment
- Deployment steps are a bit manual...

