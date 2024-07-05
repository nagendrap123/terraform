infrastructure
=============
infra is very important to create a business

Disadvantages
---------------
1.manually created
2.time taken
3.follow the sequence
  create the sg
  create the ec2
  create r53 record
4.we need to check each and every resource and note down manually
5.cost analysis 
 
Iaas --- Infra as a code 
-------------------
1.version control --> we can maintain different version of infra
multiple persons can be colleborate to create infra
2.same infra across environments -->DEV,QA,PROD
working in DEV, failed in prod 
run the same code in all environments
that creates same infra everywhere 
3. CRUD 
4.inventory --> list of resources for the project in terms of infra.
5.dependancy--> dependancies would be automatically resolve while CRUD 
6.cost analysis--> creation and deletion takes less time, so cost can be reduced
7. code reuse: modules, you can reuse the infra code created multiple times for different 
projects
8. state management--> implicit feature 

Terraform 
----------------
HCL ---> Hashi corporation language

ec2 instance creation
=====================
1.security group 
2.ec2 instance creation 

terraform works with providers 
we are using AWS provider
so we should inform to the terraform we are using AWS 
1.provider configuration
--------------------------
terraform {
  required_providers {
    aws = {
      source = "hashicorp/aws"
      version = "5.57.0"
    }
  }
}

provider "aws" {
  # Configuration options
}

2.provide aws authentication details 
-----------------------------------
By using IAM user, to create access_key and secret_key 
aws configure --> aws cli already installed. so we can run aws configure in windows 
access key
xxxxxxxxx
secret key 
xxxxxxxxxxxxxxxxxx

command line interface
--------------------
C:\Users\nagen>aws configure
AWS Access Key ID [****************S6W2]: xxxxxxxxxxxxxxxxxxxx
AWS Secret Access Key [****************qxzo]: xxxxxxxxxxxxxxxxxx
Default region name [ap-south-1]: us-east-1
Default output format [None]:

provider "aws" {
  # Configuration options
}
we can also provide access details terraform aws details 
but that is not good practice we are getting alerts from git hub 
so we are providing only region details
provider "aws" {
  region = "us-east-1"
}
syntax
==========
resource <resource type> <resource name>
mandatory 
----------
resource
resource type 
we cannot change the names

security group creation
--------------------------
ingress {
from port = 0
to port = 0
protocol  = -1
}
0 - means all ports 
-1 = means all protocols
