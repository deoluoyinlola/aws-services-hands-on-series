## Description
A demo where I migrated a simple web application (wordpress) from an on-premises environment into AWS. The on-premises environment is a virtual web server (simulated using EC2) and a self-managed mariaDB database server (also simulated via EC2). I have section this project into 4 steps and is replicas of Adrian Cantrill serverless project, [Original project link](https://github.com/acantril/learn-cantrill-io-labs)

![Architecture](Docs/database-migration/ARCHITECTURE-OVERALL.png)

* [Pre-requisites](#pre-requisities)
* [Provision the environment and review tasks](#Provision-the-environment-and-review-tasks)
* [Establish Private Connectivity Between the environments (VPC Peer)](#stablish-Private-Connectivity-Between-the-environments-(VPC-Peer))
* [Create & Configure the AWS Side infrastructure (App and DB)](#Create-&-Configure-the-AWS-Side-infrastructure-(App-and-DB))
* [Migrate Database & Cutover](#Migrate-Database-&-Cutover)
* [Cleanup the account](#Cleanup-the-account)

## Pre-requisites
- [aws](https://aws.amazon.com/) - cloud platform, offers reliable, scalable, and inexpensive cloud computing services.

## Provision the environment and review tasks
![STAGE1](Docs/database-migration/STAGE1.png)

## Establish Private Connectivity Between the environments (VPC Peer)
![STAGE2](Docs/database-migration/STAGE2.png)

## Create & Configure the AWS Side infrastructure (App and DB)
![STAGE3](Docs/database-migration/STAGE3.png)

## Migrate Database & Cutover
![STAGE4](Docs/database-migration/STAGE4.png)

## Cleanup the account

