## How CloudFormation Works

Nested stacks show how CloudFormation works

![Create request and response messages through nested stacks](images/nested-stacks/create-messaging.dot.svg)

Note:
Messages and responses flow asynchronously from parent to child and back again.
Update-stack and delete-stack work the same way.
