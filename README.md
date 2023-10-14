# terraform-serverless-rest-api-dynamodb
Lambda based REST API entirely through code - API Gateway, YAML &amp; Terraform
![image](https://github.com/joelwembo/terraform-aws-serverless-rest-api-dynamodb/assets/19718580/cb96a7e8-6649-44a6-948f-9d147e4f6bdf)

Serverless Applications with AWS Lambda and API Gateway

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
--no-aws-s3-accelerate Explicitly disables S3 Transfer Acceleration. It also requires additional s3:PutAccelerateConfiguration permissions..

# Compilation

sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket $SAM_CODE_BUCKET

- terraform init

- terraform plan

- terraform deploy

- terraform destroy

