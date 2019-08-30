# Lambda Engine CheckOut
EvoX Engine Lambda CheckOutV2

Requirements:
- VPC
- Python 3.7

Env variables:
```
EVO_REGION={staging, production}
APP_ENV={AWS_REGION}
```

Setup for deployments
- Install Serverless running `npm install -g serverless`

To deploy:
- Clone the repository
- Run `sh compress.sh`
- Configure your default AWS credentials running the command `serverless config credentials --provider aws --key {AWS_KEY} --secret {AWS_SECRE_KEY}`
- Deploy command `serverless deploy --stage {STAGE} --region {AWS REGION} --aws-profile {LOCAL AWS PROFILE}` OR using the AWS API key `serverless deploy --stage {STAGE} --region {AWS REGION} --aws-profile {LOCAL AWS PROFILE} --provider aws --key {AWS_KEY} --secret {AWS_SECRE_KEY}`

* Make sure your user has permission to handle Lambda and API Gateway. *

Deploy sample to staging
`serverless deploy --stage staging --region eu-west-1 --aws-profile default`
