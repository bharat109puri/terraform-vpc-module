AWS VPC Terraform module
========================

Terraform module which creates VPC resources on AWS.

These types of resources are supported:

* VPC
* Public Subnet
* Private Subnet
* Route table
* Internet Gateway
* NAT Gateway

Usage
-----

```hcl
module "vpc" {
  source = "/vpc/aws"

  name = "my-vpc"
  vpc_cidr = "10.0.0.0/16"

  private_subnets = ["10.0.1.0/24", "10.0.2.0/24", "10.0.3.0/24"]
  public_subnets  = ["10.0.101.0/24", "10.0.102.0/24", "10.0.103.0/24"]

  enable_nat_gateway = true

  tags = {
    Creator = "Terraform"
    Environment = "staging"
  }
}
```



Terraform version
-----------------

Terraform version 0.10.3 or newer is required for this module to work.


Tests
-------
## How to test

```bash
terraform get
terraform validate
terraform plan
```

## How to apply

```bash
terraform apply
```

## How to destroy

```bash
terraform destroy
```



Authors
-------

Module managed by [Bharat Puri](https://github.com/bharat109puri).
Contact at : bhpuri@gmail.com for support and consulting
