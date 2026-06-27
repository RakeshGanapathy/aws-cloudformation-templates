# AWS CloudFormation Templates

Production-ready AWS CloudFormation templates for common infrastructure patterns — ECS Fargate, EC2, Lambda, S3, KMS.

---

## Templates

| Template | Description |
|---|---|
| `ECS/` | ECS Fargate service with ALB, auto-scaling, and ECR integration |
| `EC2/` | EC2 instance with security groups and IAM role |
| `Lambda/` | Lambda function with IAM execution role and CloudWatch logging |
| `S3/` | S3 bucket with versioning, encryption, and bucket policy |
| `KMS/` | KMS key with key policy for S3/RDS encryption |

---

## Usage

```bash
# Deploy a stack
aws cloudformation deploy \
  --template-file ECS/fargate-service.yml \
  --stack-name my-ecs-stack \
  --capabilities CAPABILITY_IAM \
  --parameter-overrides Environment=prod

# Validate a template
aws cloudformation validate-template \
  --template-body file://ECS/fargate-service.yml
```

---

## Prerequisites

- AWS CLI configured with deploy permissions
- Existing VPC and subnets (most templates take these as parameters)

---

## Stack

`AWS CloudFormation` `ECS Fargate` `EC2` `Lambda` `S3` `KMS` `IAM`

