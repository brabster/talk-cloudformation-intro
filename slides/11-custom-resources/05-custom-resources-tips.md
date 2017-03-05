## Custom Resources

Some tips...

- Use standard resources where you can
- Use libs to help write custom resources
- Ensure S3 access in private subnets
- Think about how to manage your custom resources
- Implement with AWS Lambda, not SNS + EC2
- Think idempotently and defensively
- Be aware of PhysicalResourceId and "replacement" on update

Note:
- Standard AWS CloudFormation resources are battle tested - but even they sometimes have bugs!
- Error handling isn't the best - if you fail to write the response correctly you will be waiting a long time for a timeout
- If you don't provide access to S3, you'll again get a long timeout
- Custom Resources will need to be there before you use them, but they're not explicit dependencies
- SNS + EC2 is the old, hard way. AWS Lambda is relatively simple and easier to implement
- Assume at-least-once invocation and code accordingly
- Think about your error handling strategy
- Returning a different PhysicalResourceId on update triggers a delete of the old physical resource ID
- Replacement behaviour only documented in http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-custom-resources-sns.html
