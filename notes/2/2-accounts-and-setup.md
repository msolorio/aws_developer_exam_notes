## Root User
- logs in with email and password
- set up MFA
- Root account has full permissions
- Cannot be restricted
- Best practice
  - don't use root user
  - create IAM user for use instead

## IAM User
- Entity that represents a person or service
- IAM Policy can be associated with a user
- Set up MFA

- User can be assigned
  - access keys to access to CLI and SDK
  - password for access to management console

- IAM users can be created to represent applications - service accounts
- can have up to 5000 users per AWS root account

- Each IAM user has
  - friendly name
  - Amazon Resource Name (ARN)

- Best practice
  - one account per user
  - Can set password policy to set password complexity

---

## IAM Group
- contain many users
- IAM policy can be assigned to a group
- groups cannot be nested

---

## IAM Role
- Assumed by a trusted entity
- IAM policy assigned to a role
- used by services to allow service to act on your behalf

---

## IAM Policy

- document that defines permissions
- can be applied to users, groups, roles
- written in json
- all permissions are denied by default
- can use conditional statements in a policy
  - ie. only apply if caller has this IP address

---

## Authenticaion Methods

IAM Access Key
- access key ID (public)
- secret access key (private)
- users can be given ability to change access keys
- Root user can disable access keys

Password
- Allows AIM user to sign in to console
- Can allow users to change their own passwords
- Can use a policy to allow only certain users to change their password

IAM Server Certificate / Signing Certificate
- SSL/TLS certificate to authenticate with some services
- can use AWS Certificate Manager to manage server certificates

---

## MFA

- Something you know (password)
- Something you have (smart phone)
- Something you are (biometric, fingerprint)

MFA with AWS invloves the first 2
- password
- Code from MFA device (app on phone)

Security Token Service
- enables you to request temporary, limited privilege credentials for IAM users

---
