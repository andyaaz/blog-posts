# AWS checklist

Practical things I always forget and spend time googling and looking in AWS doc

## Root account set up

- Security
  - [MFA](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html#enable-virt-mfa-for-root)
- Operation (make life easier)
  - [Allow IAM user access billing info](https://aws.amazon.com/premiumsupport/knowledge-center/iam-billing-access/)
  - [Receive billing PDF monthly](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/emailed-invoice.html)
  - [Create account alias](https://docs.aws.amazon.com/IAM/latest/UserGuide/console_account-alias.html#CreateAccountAlias)
  - [Create IAM admin](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
  - [Alternate contacts](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/manage-account-payment.html#manage-account-payment-alternate-contacts)

## IAM admin set up

- Security
  - [MFA](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa_enable_virtual.html#enable-virt-mfa-for-root)
- Operation
  - [CloudWatch Billing Alarm](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html)

## Management-Prod-Dev accounts set up

[It is a best practice to have mulitple account for different environments](https://docs.aws.amazon.com/whitepapers/latest/organizing-your-aws-environment/organizing-your-aws-environment.html)

- [switch roles from iamadmin in console](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-console.html)
- [switch roles from iamadmin in cli](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-cli.html)
