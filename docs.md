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
