# terraform-serverless-rest-api-dynamodb
Lambda based REST API entirely through code - API Gateway, YAML &amp; Terraform

Serverless Applications with AWS Lambda and API Gateway
Serverless computing is a cloud computing model in which a cloud provider automatically manages the provisioning and allocation of compute resources. This contrasts with traditional cloud computing where the user is responsible for directly managing virtual servers.

A popular approach to running "serverless" web applications is to implement the application functionality as one or more functions in AWS Lambda and then expose these for public consumption using Amazon API Gateway.

This guide will show how to deploy such an architecture using Terraform. The guide assumes some basic familiarity with Lambda and API Gateway but does not assume any pre-existing deployment. It also assumes that you are familiar with the usual Terraform plan/apply workflow; if you're new to Terraform itself, refer first to the Getting Started guide.

This is a slightly-opinionated guide, which chooses to ignore the built-in versioning and staged deployment mechanisms in AWS Lambda and API Gateway. In many cases these features are not necessary when using Terraform because changes can be tracked and deployed by keeping the Terraform configuration in a version-control repository. It also uses API Gateway in a very simple way, proxying all requests to a single AWS Lambda function that is expected to contain its own request routing logic.


# Compilation

sam package --template-file sam-template.yaml --output-template-file sam-deploy.yaml --s3-bucket $SAM_CODE_BUCKET


>sam package --template-file sam-template.yaml --output-template-file sam-deploy.yaml --s3-bucket prodxcloud-terraform-state
        Uploading to 823a67346e42ff8e68d81d8c3e069934  1412112 / 1412112  (100.00%)
        Uploading to c19477640ae82382c23af8c9f5937a93  868 / 868  (100.00%)
        Uploading to 1a265dc3297bf39f7edd961edf2a5e24  715 / 715  (100.00%)

terraform init

terraform plan

terraform deploy

api_invoke_url = "https://zdzvs65nih.execute-api.ap-southeast-1.amazonaws.com/v1/getdata"
api_key = "HVXHIoUnZ57Y0j28UHwPr1dQr71W3DXa9A44KLIW"

curl -v -H "x-api-key=7CRG1Ms1Su3BTzdzexFJY5ZdbHrZiER1XoiCVa17"  GET  https://zdzvs65nih.execute-api.ap-southeast-1.amazonaws.com/v1/getdata

curl -v -H X-API-TOKEN=7CRG1Ms1Su3BTzdzexFJY5ZdbHrZiER1XoiCVa17 GET 'https://fqzpyg5ond.execute-api.ap-southeast-1.amazonaws.com/v1/getdata'

curl 'https://fqzpyg5ond.execute-api.ap-southeast-1.amazonaws.com/v1/getdata?apikey=7CRG1Ms1Su3BTzdzexFJY5ZdbHrZiER1XoiCVa17'

