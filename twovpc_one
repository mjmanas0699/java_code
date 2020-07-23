provider "aws" {
  region  = "ap-south-1"
  profile = "manas" 
}

variable "two_with_one" {
  type =  "list"
  default     = [ "10.0.0.0/16" ,"10.10.0.0/16" ]

}
resource "aws_vpc" "main" {
for_each = toset(var.two_with_one)
cidr_block = each.value
instance_tenancy = "default"
tags = {
       Name = "VPC ${each.value}" 
       }
} 
