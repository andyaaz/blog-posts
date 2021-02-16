---
title: "AWS Services Overview"
description: "Overview of some AWS services"
slug: "aws-services-overview"
createdAt: "2021-02-14"
tags: ["aws"]
---

Five pillars references:
- P (1)
- R
- O
- C
- S

## S3 and Glacier(R)

- designed for 11 9s durability 
- Replica in multiple AZs cross-region (DR) >= 3
- Life cycle policies
  - e.g. standard -> standard IA -> Glacier -> delete
- Help you meet RTO and RPO
- Encrytion: SSE-S3, SSE-KMS, SSE-C

|                                 | standard     | standard IA    | Glacier        |
|---------------------------------|--------------|----------------|----------------|
| availability SLA                | 99.9         | 99             | 99.9           |
| resilience                      | cross region | same           | same           |
| availability                    | 4 9s         | 3 9s           | x              |
| minimum storage duration charge | x            | 30 days        | 90 days        |
| Retrieval time                  | x            | x              | up to 12 hrs   |
| Retrieval fee                   | x            | charged per GB | charged per GB |

## Snowball, Snowball Edge and Snowball Mobile (R)

- Physical storage and compute(Edge)
- Help with locations with inconsistent network connectivity
- Petabyte data transport
- Harsh environments (rugged)

## CloudFront (P)

P
- read from S3 
- upload to S3 with backbone network instead of public internet

## EC2

### Auto-scaling groups

## Lambda

## CloudWatch

### CloudWatch Logs

## CloudTrail

## RDS (P, R)

- Aurora (mysql and postgres compatible, faster than both)
- Microsoft Mysql Server
- Oracle
- Maria DB
- Postgresql
- Mysql

- auto backup
- snapshots(user-initiated, stored in S3)
- Multi-AZ deployments
- automatic replacing compute instance in the event of hardware failure

- push-button scale up or down(up to 32 vCPUs and 244GiB RAM)
- Aurora handles storage scaling 
- read replica (mysql, mariadb, postgres, oracle and aurora)

when to use: 
- transactional data
- complex query

## DynamoDB (P)

- no-sql db
- scaling managed by aws
- no need to choose size when setting up

when to use:
- simple read/write 
- a single payload is less 4KB

## Redshift 

- sql db
when to use: 
- analystical data

## CloudFormation

## ElastiCache (P)

P
- two options: 

|                                                          | Memcached | Redis |
|----------------------------------------------------------|-----------|-------|
| Multitreaded                                             | Y         | N     |
| Advanced data structures                                 | N         | Y     |
| Snopshots, replication, Pub/Sub, Lua, Geospatial support | N         | Y     |
  
[learn more](https://aws.amazon.com/elasticache/redis-vs-memcached/)

## Elastic File System (P)

- can be mounted on multiple EC2 instances
- relatively expensive
- highly scalable

## Elastic Block Storage (P)

- not scalable, need to manually scale size
- can be mounted on ONE EC2 instance at a time
- two options: HDD/SSD
- Use provisioned IOPS for better performance

## Elastic Load Balancing

## Elastic IP

## Route 53

## VPC

### Security Groups

### Network Access Control List

### Route Tables

### Internet Gateway

### NAT(Network Address Translation)

### Flow Logs

## API Gateway

## System Manager

### Session manager

## Direct Connect (P)

- have direct connection between on-premises infra and aws

## Transit Gateway

- connects multiple VPCs through a central place so that they can talk to each other easily

## IAM (Identity Access Management)

### Roles

## Cognito

### User pool

### Identity pool

## SQS

### Dead-letter Queue

## SNS

## Elastic Beanstalk

## Storage Gateway

- send on-premises data to S3 (extremely fast)

## Organization

## Control Tower

## Amazon Machine Images
