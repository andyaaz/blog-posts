---
title: "AWS IAM key concepts"
description: "AWS IAM key concepts"
slug: "aws-iam-key-concepts"
createdAt: "2021-02-14"
tags: ["aws"]
---

IAM functions

- manage identities (create, delete users)
- authenticate (email+password, access key+secret)
- authorize (through policies)

Components

- users
  - when you know who will use it (most likely a human)
- groups
  - group users together (developers, admins)
- roles
  - when you don't know who will use it
  - used by whoever needs it
