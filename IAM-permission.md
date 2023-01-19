!Note that all the files, images and architecture reference are find inside cfncustom-resources dir of Docs dir.;
![CFCustomResourcesArch.png](Docs/IAM-permission/CFCustomResourcesArch.png)

In this DEMO lesson;
* [Goals](#goals)
* [IAM User](#IAM-User)
* [IAM Group](#IAM-Group)

## Goals
I create an IAM user, group and experiment with assigning permissions on two S3 buckets via inline policies and managed policies.

## IAM User
The DEMO lesson will require two browsers
- the 1st will login to the IAMADMIN user of the general account
- the 2nd will login to an IAM user called 'deolu' for testing.

### Upload Image to S3 Bucket
- I will not set any particular hard-coded name in the cfn, so it will automatically generate resources name.
![IAM-User](Docs/IAM-permission/IAM-User.png)

- Open up deolu user, under resource, leading to IAM console. Discover it is aws managed policy
![IAM-User](Docs/IAM-permission/Confirm-Policy.png)

From here, > Dashboard > copy the, Sign-in URL for IAM users in this account, from the right hand > In another browser, paste the link https://950689934615.signin.aws.amazon.com/console

Move to s3 bucket console in the 'iam-animal' to upload the pic;
![IAM-User](Docs/IAM-permission/animal.png)

Repeat same process for iam-cat;
![IAM-User](Docs/IAM-permission/cat.png)

### Set and Change Permission
From IAM console; User >  IAM-User-deolu-... > Add Permissions > Attach existing policies directly > AllowAllS3ExceptCats > Next; Review > Add Permissions

![IAM-User](Docs/IAM-permission/s3permit.png)

## IAM Group
How groups can be used to hold permissions for group members.

From the admin IAM User account and N. Virginia region;
Enter Cloudformation console;
Create stack > Template is ready > Upload file > (select the right file, I used demo_cfn.yaml) > Enter stack name and password > Next > Acknowledge > Submit
