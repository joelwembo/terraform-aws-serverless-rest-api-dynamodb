# terraform-serverless-rest-api-dynamodb
Lambda based REST API entirely through code - API Gateway, YAML &amp; Terraform
![image](https://github.com/joelwembo/terraform-aws-serverless-rest-api-dynamodb/assets/19718580/cb96a7e8-6649-44a6-948f-9d147e4f6bdf)


Serverless Applications with AWS Lambda and API Gateway
Serverless computing is a cloud computing model in which a cloud provider automatically manages the provisioning and allocation of compute resources. This contrasts with traditional cloud computing where the user is responsible for directly managing virtual servers.

serverless deploy
Options
--config or -c Name of your configuration file, if other than serverless.yml|.yaml|.js|.json.
--stage or -s The stage in your service that you want to deploy to.
--region or -r The region in that stage that you want to deploy to.
--package or -p path to a pre-packaged directory and skip packaging step.
--verbose Shows all stack events during deployment, and display any Stack Output.
--force Forces a deployment to take place.
--function or -f Invoke deploy function (see above). Convenience shortcut - cannot be used with --package.
--conceal Hides secrets from the output (e.g. API Gateway key values).
--aws-s3-accelerate Enables S3 Transfer Acceleration making uploading artifacts much faster. You can read more about it here. It requires additional s3:PutAccelerateConfiguration permissions. Note: When using Transfer Acceleration, additional data transfer charges may apply.
--no-aws-s3-accelerate Explicitly disables S3 Transfer Acceleration. It also requires additional s3:PutAccelerateConfiguration permissions.

A popular approach to running "serverless" web applications is to implement the application functionality as one or more functions in AWS Lambda and then expose these for public consumption using Amazon API Gateway.

This guide will show how to deploy such an architecture using Terraform. The guide assumes some basic familiarity with Lambda and API Gateway but does not assume any pre-existing deployment. It also assumes that you are familiar with the usual Terraform plan/apply workflow; if you're new to Terraform itself, refer first to the Getting Started guide.

This is a slightly-opinionated guide, which chooses to ignore the built-in versioning and staged deployment mechanisms in AWS Lambda and API Gateway. In many cases these features are not necessary when using Terraform because changes can be tracked and deployed by keeping the Terraform configuration in a version-control repository. It also uses API Gateway in a very simple way, proxying all requests to a single AWS Lambda function that is expected to contain its own request routing logic.
![image](https://github.com/joelwembo/terraform-aws-serverless-rest-api-dynamodb/assets/19718580/ffe4a762-9ef1-4d4d-854e-40f9aa9682b1)

# Compilation

sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket $SAM_CODE_BUCKET


terraform init

terraform plan

terraform deploy
