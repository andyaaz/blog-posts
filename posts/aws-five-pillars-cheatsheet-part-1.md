---
title: "AWS Five Pillars Cheatsheet Part 1"
description: "Learning notes of AWS five pillars"
slug: "aws-five-pillars-cheatsheet-part-1"
createdAt: "2021-02-13"
tags: ["aws"]
---

## Intro

I am preparing for my AWS solution architect exam and here are some refreshers I might need later. I write things as concise and easy for me to understand as possible so they might not be case for everyone else, sorry. I think that the concepts mentioned might still be useful when I work on actual projects so I decided to share here. For full/more detailed version, please visit [AWS Exam Prep](https://aws.amazon.com/certification/certification-prep/)

## Resillent Architectures

- services:

  - Elastic Load Balancers
  - EFS
  - S3
    - storage classes: standard, standard infrequent
    - Encryption: SSE-S3, SSE-KMS, SSE-C(customer managed)
    - unlimited storage
    - highly durable (11 9s)
    - region scoped
  - Glacier (pretty much S3, but for archives)
    - often used with life cycle policy with s3
    - highly durable (11 9s)
    - access: bulk(cheap 12hrs), expedited(more expensive, 5 mins)
  - Lambda
    - stateless code with managed compute units (without EC2 and auto scaling groups)

- key ideas:

  - strongly consistent vs eventually consistent
  - s3 new object is strongly consistent and update is eventually consistent (you will read new objects immediately but not so after update/delete)
  - decoupling (one failing service should not affect other services. everything fails and failures should be expected)
    - direct call vs SQS/load balancer
    - Elastic IP (keep failing and new server IP the same)
  - RTO: recovery time objective (how much time it takes to recover)
  - RPO: recovery point objective (how much data is lost measured in time)

- axioms for the test:
  - "single az" is never correct
  - AWS managed services should be preferred
  - Fault-tolerant: self-healing (failures do not impact users)
  - High Availability: e.g. 11 9s (ok to fail)
  - everything fails, all the time

## Performant Architectures

- services:

  - EBS
    - HDD: cold, throughtput(faster)
      - sequensial access
    - SSD: general, provisioned IOPS(faster)
      - random access
  - RDS
    - complex transactions
    - NO read replica for Microsoft SQL server and Oracle
  - DynamoDB
    - auto sharding
    - fast read and write
  - Redshift (SQL interface, analystical data, not transactional)
  - ElastiCache
    - Memcached: simple
    - Redis
  - CloudFront
    - static / dynamic(will go through aws backbone network instead of public internet)
  - Auto Scaling (group)
    - use case: any service -> CloudWatch -> alarm -> Auto Scaling Policies

- key ideas:
  - no static content on servers, put them on S3
  - db
  - caching
  - scale in/out(horizontal) vs scale up/down (vertical)

## Operational Excellence

- services:

  - CloudWatch
  - VPC Flow logs
  - CloudFormation
  - Config
  - Inspector
  - CloudTrail
  - Trusted Advisor

- key ideas:

  - infra code (so that it can be reviewed and tracked)
  - monitoring

- axioms for the test:
  - IAM over key + password
  - monitoring metrics
  - automate responses to metrics (and provide alerts for unusual events)
