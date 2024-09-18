# S3 Backend Module
This module sets up a S3 bucket (backend) for storing (and sharing) states of infrastructures being provisioned by Terraform. The backend can be used to store the state files of different deployments (organized by 'key'), and the design uses a DynamoDB table for locking (so that only one actor can run Terraform to modify the instructure at any time).

## Usage
```
module "s3backend" {
  source  = "skwokie/s3backend/aws"
  version = "0.1.1"
  namespace = "change_this"
}
```

## Reference
https://developer.hashicorp.com/terraform/language/backend/s3
https://www.manning.com/books/terraform-in-action
