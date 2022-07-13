
# CDK EC2 Instance Stack with Custom Resource Tags 

This repo will create EC2 Instance in new VPC with Systems Manager enabled and tag the resources for cost-optimization

This code is based on the [example CDK code project](https://github.com/aws-samples/aws-cdk-examples/tree/master/python/ec2/instance).

This example includes:

* Own VPC with public subnet (following AWS Defaults for new accounts)
* Based on latest Amazon Linux 2
* System Manager replaces SSH (Remote session available trough the AWS Console or the AWS CLI.)
* Userdata executed from script in S3 (`configure.sh`)
* Tag the AWS resources with custom tags

## Useful commands

 * `cdk bootstrap`   initialize assets before deploy
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack to your default AWS account/region
 * `aws ssm start-session --target i-xxxxxxxxx` remote session for shell access
