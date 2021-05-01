---
title: "AWS Default VPC"
description: "AWS Default VPC"
slug: "aws-default-vpc"
createdAt: "2021-02-15"
tags: ["aws"]
---

The default VPC

- created by AWS, can be removed. can be recreated easily.
- don't do any serious deployment in it. use a custom one

In a newly created AWS account, in every region(e.g. ap-southeast-1) there will be a default VPC and 
- all default VPCs has CIDR of 172.31.0.0/16
- one subnet for each AZ (if region is ap-southeast-1, AZ will ap-southeast-1a)
- subnet CIDR will be /20 (meaning 2^12=4096 number of private IP addresses in a subnet, e.g. 172.31.0.0/20, 172.31.16.0/20, ...)
- in subnets will default give EC2 public IP 
- Internet Gateway (allows internet access both in and out)
- security group (stateful)
- Network Access Control List (stateless)

so it's region resilient
