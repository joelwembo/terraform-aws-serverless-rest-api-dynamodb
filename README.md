# terraform-serverless-rest-api-dynamodb
Lambda based REST API entirely through code - API Gateway, YAML &amp; Terraform
![image](https://github.com/joelwembo/terraform-aws-serverless-rest-api-dynamodb/assets/19718580/cb96a7e8-6649-44a6-948f-9d147e4f6bdf)

Serverless Applications with AWS Lambda and API Gateway

# Compilation

sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket $SAM_CODE_BUCKET

- terraform init

- terraform plan

- terraform deploy

- terraform destroy

