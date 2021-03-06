# `awsmaniac-vpc-example`

## What is it?

It is an example for *AWS VPC* that I have prepared for the live stream session for [AWS Maniac](https://awsmaniac.com/live).

## Live Stream 2: Amazon VPC and AWS Networking

### Terraform

#### Usage

1. `make`
2. `source ./.env/bin/activate`
3. `aws-mfa --profile=<YOUR_PROFILE>`
4. `export AWS_DEFAULT_PROFILE=<YOUR_PROFILE>` - of course you should choose the one you want.
5. `export AWS_DEFAULT_REGION=eu-north-1` - of course you should choose the one you want.
6. `(cd remote-state && terraform-init)`
7. `(cd remote-state && terraform apply)` - one time operation, if you do not have backend configured.
8. `(cd vpc && terraform-init && terraform apply)`

### AWS CloudFormation

1. `make`
2. `source ./.env/bin/activate`
3. `aws-mfa --profile=<YOUR_PROFILE>`
4. `export AWS_DEFAULT_PROFILE=<YOUR_PROFILE>` - of course you should choose the one you want.
5. `export AWS_DEFAULT_REGION=eu-north-1` - of course you should choose the one you want.
6. ``aws cloudformation create-stack --stack-name "CF-DEV-VPC-EXAMPLE" --template-body "file://`pwd`/livestream-2-aws-networking/cloudformation/vpc.template.yaml"``

## License

- [MIT](LICENSE.md)

## Authors

- [Wojciech Gawroński (afronski) - AWS Maniac](https://github.com/afronski)
