---
title: "AWS root accounts set up"
description: "AWS root accounts set up"
slug: "aws-root-accounts-set-up"
createdAt: "2021-02-14"
tags: ["aws"]
---

Things to remember
- create root accounts for different env (PROD, DEV, STAGING)
- create admin IAM accout(s) for each env
- send monthly report to email
- set up billing alerts(CloudWatch) and enable admin IAM to access billing dashboard (must enable explicitly)
  - create BillingAlert topic with SNS
- never use root accounts to do things
  - it's IMPOSSIBLE to restrict permissions on root account. You are Fxxked if root user is compromised.
- enable MFA for root accounts (can use google authenticator)
- enable MFA for admin IAM accounts (can use google authenticator)
- add addtional billing contacts

Tricks
- generate multiple email address with gmail "+" trick (format: gmail-address-prefix+whatever@gmail.com)
- set a custom IAM login url

