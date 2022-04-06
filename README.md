## Terraform VPC Module

#### Resources Provisionados
 ##### - VPC
 ##### - Subnets
 ##### - Internet Gateway
 ##### - Nat Gateway
 ##### - Route Table
 ##### - Elastic IP

```
variable "name" {}
variable "environment" {}
variable "region" {}
variable "cidr_block" {}
variable "availability_zones" {}
variable "tags" {}
variable "routes" {}

module "vpc" {
  source             = "github.com/opsteamhub/terraform-vpc-module.git"
  name               = var.name
  environment        = var.environment
  region             = var.region
  cidr_block         = var.cidr_block
  availability_zones = var.availability_zones
  tags               = var.tags
  routes             = var.routes 
}

```