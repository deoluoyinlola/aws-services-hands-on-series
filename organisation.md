!Note that all the files, images and architecture reference are find inside IAM-permission dir of Docs dir.;
![CFCustomResourcesArch.png](Docs/IAM-permission/CFCustomResourcesArch.png)

In this DEMO lesson;
* [Goals](#goals)
* [AWS Organisation](#AWS-Organisation)
* [Service Control Policies](#Service-Control-Policies)

## Goals
In this hands-on I will create an organisation for a business. The GENERAL account will become the MASTER account for the organisation.
I will invite the PRODUCTION account as a MEMBER account and create the DEVELOPMENT account as a MEMBER account.

Finally - I will create an OrganizationAccountAccessRole in the production account, and use this role to switch between accounts.

## AWS Organisation
- Requirement; Other additional AWS accounts say Production and Develop account, Set up additional browser.
- Login into the General AWS account, select N. Virginia region


## Service Control Policies