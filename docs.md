# Compilation

sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket $SAM_CODE_BUCKET


>sam package --template-file template.yaml --output-template-file deploy.yaml --s3-bucket prodxcloud-terraform-state
        Uploading to 823a67346e42ff8e68d81d8c3e069934  1412112 / 1412112  (100.00%)
        Uploading to c19477640ae82382c23af8c9f5937a93  868 / 868  (100.00%)
        Uploading to 1a265dc3297bf39f7edd961edf2a5e24  715 / 715  (100.00%)

terraform init

terraform plan

terraform apply

Apply complete! Resources: 7 added, 1 changed, 1 destroyed.

Outputs:

api_invoke_url = "https://te6m07xnvk.execute-api.ap-southeast-1.amazonaws.com/v1"
api_key = "2aJbmhqasy5JAyfKpOtmUDQwWRTctFiad1iLARgc

curl -v -H "x-api-key=2aJbmhqasy5JAyfKpOtmUDQwWRTctFiad1iLARgc"  GET  https://te6m07xnvk.execute-api.ap-southeast-1.amazonaws.com/v1/getdata

curl -v -H X-API-TOKEN=2aJbmhqasy5JAyfKpOtmUDQwWRTctFiad1iLARgc GET 'https://te6m07xnvk.execute-api.ap-southeast-1.amazonaws.com/v1/getdata'

curl 'https://fqzpyg5ond.execute-api.ap-southeast-1.amazonaws.com/v1/getdata?apikey=7CRG1Ms1Su3BTzdzexFJY5ZdbHrZiER1XoiCVa17'
