# Security Best Practices

### Use IAM to control access <a href="#use-iam-to-control-access" id="use-iam-to-control-access"></a>

IAM is an AWS service that you can use to manage users and their permissions in AWS.&#x20;

Users require full access to manage all of the resources in a template.&#x20;

AWS CloudFormation makes calls to create, modify, and delete those resources on their behalf. To separate permissions between a user and the AWS CloudFormation service, use a service role. AWS CloudFormation uses the service role's policy to make calls instead of the user's policy.

To deploy this product IAMRoleForStackCreation is required for the user

For more information, see [AWS CloudFormation service role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-servicerole.html).

Follow the principle of least privilege as described in this [link](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege)

