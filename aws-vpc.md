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
[AWS-VPC-Option](https://d1.awsstatic.com/whitepapers/aws-amazon-vpc-connectivity-options.pdf)

- VPC Capacity Formulation Plan Example; 1.)Number of AWS regions the business will operate in., 2.)How many AZs(for resilient) will the VPC use(say at least 3) & tiers - subnet, 3.) e.g 16/ VPC - 4AZs, 4tiers - 16 subnets. Where 16 subnets = /20 per subnet(4091IPs)
![vpc](Docs/vpc/vpc-formular.png)

## Create VPC
- Login into the Management AWS account, select N. Virginia region
- From the find service box, type `VPC` to move to vpc console, click on `Your VPCs` Click on `Create VPC` Decide and choose which resource to create from `VPC Settings`, here - VPC only, then give it a name; a4l-vpc1, set the IP range - CIDR, Select `Amazon-provided...` for IPv6 CIDR block so that it will be enable for IPv6. Maintain the tenancy at default or if desire can change but factor cost. Every other thing remain default. > Click `Create VPC`
![vpc](Docs/vpc/vpc-cr8.png)
- From the just created VPC, Select `Action` dropdown > Choose `Edit VPC Setting` > Enable all setting under `DNS setting` > Click on `Save`

## VPC Subnet
- Use the calculator below to get the appropriate IP addresses
[Subnet Calculator](https://www.site24x7.com/tools/ipv4-subnetcalculator.html)
- For convience, here are the IP addresses;
```
NAME CIDR AZ CustomIPv6Value

sn-reserved-A 10.16.0.0/20 AZA IPv6 00
sn-db-A 10.16.16.0/20 AZA IPv6 01
sn-app-A 10.16.32.0/20 AZA IPv6 02
sn-web-A 10.16.48.0/20 AZA IPv6 03

sn-reserved-B 10.16.64.0/20 AZB IPv6 04
sn-db-B 10.16.80.0/20 AZB IPv6 05
sn-app-B 10.16.96.0/20 AZB IPv6 06
sn-web-B 10.16.112.0/20 AZB IPv6 07

sn-reserved-C 10.16.128.0/20 AZC IPv6 08
sn-db-C 10.16.144.0/20 AZC IPv6 09
sn-app-C 10.16.160.0/20 AZC IPv6 0A
sn-web-C 10.16.176.0/20 AZC IPv6 0B

Remember to enable auto assign ipv6 on every subnet you create.
```
- From the VPC, select `Subnets` > click `Create Subnet` > Choose the right VPC ID from the dropdown > Populate and add more 3 subnet in the Subnet Settings > Click `Create Subnet`. Repeat the above steps for the next subnet - AZ-b, repeat one more time for the last subnet - AZ-c with the above info for each subnet creations.
![vpc](Docs/vpc/vpc-subnet.png)

### Manually Set auto assign ipv6
Select each subnet and click on > Click on `Action` > Choose `Edit Subnet Setting` > Check `Enable auto-assign ipv6 address` > click on `Save`. Repeat the same process for other 11 subnets.