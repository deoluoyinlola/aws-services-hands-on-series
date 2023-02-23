!Note that all the files, images and architecture reference are find inside vpc dir of Docs dir.;
![vpc](Docs/vpc/vpc.png)

In this DEMO lesson;
* [Goals](#goals)
* [References](#References)
* [Create VPC](#Create-VPC)
* [VPC Subnet](#VPC-Subnet)

## Goals
In this hands-on I will create an aws VPC for a business.

## References
https://d1.awsstatic.com/whitepapers/aws-amazon-vpc-connectivity-options.pdf

- VPC Capacity Formulation Plan Example; 1.)Number of AWS regions the business will operate in., 2.)How many AZs(for resilient) will the VPC use(say at least 3) & tiers - subnet, 3.) e.g 16/ VPC - 4AZs, 4tiers - 16 subnets. Where 16 subnets = /20 per subnet(4091IPs)
![vpc](Docs/vpc/vpc-formular.png)

## Create VPC
- Login into the Management AWS account, select N. Virginia region
- From the find service box, type `VPC` to move to vpc console, click on `Your VPCs` Click on `Create VPC` Decide and choose which resource to create from `VPC Settings`, here - VPC only, then give it a name; a4l-vpc1, set the IP range - CIDR, Select `Amazon-provided...` for IPv6 CIDR block so that it will be enable for IPv6. Maintain the tenancy at default or if desire can change but factor cost. Every other thing remain default. > Click `Create VPC`
![vpc](Docs/vpc/vpc-cr8.png)
- From the just created VPC, Select `Action` dropdown > Choose `Edit VPC Setting` > Enable all setting under `DNS setting` > Click on `Save`

## VPC Subnet