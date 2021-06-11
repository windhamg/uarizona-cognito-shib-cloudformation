## AWS Cognito User Pool CloudFormation Template for UArizona IdP

This project contains a CloudFormation template and corresponding parameters file for deploying a Cognito User Pool, configured to use the UA Shibboleth IdP as a federated identity provider.

### To Deploy:

  1. If not already installed, install the [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) on the system from which you will deploy the CloudFormation template.
  2. `cd` to the directory of this project in a shell
  3. Ensure your shell has the appropriate IAM credentials for deploying the CloudFormation template. You will need credentials with `Administrator` permissions.
  4. Run the following AWS CLI command to deploy the stack (or, alternatively, use the AWS CloudFormation console). You can override parameters in the template via a JSON file or directly on the command-line (see `aws cloudformation deploy help` for information):
  ```
  aws cloudformation deploy --stack-name my-cognito --template-file cognito-cf.yml --parameter-overrides file://parameters.json --region <desired-region>
  ```
  6. Once the stack has deployed, get the output values from the stack, as you'll need these for use in your client application(s).

