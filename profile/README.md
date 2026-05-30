# LocalEmu

**Run AWS locally. No account. No token. No sign-up.**

LocalEmu is a free, open-source AWS cloud emulator. Point the AWS CLI, boto3,
Terraform, or CDK you already use at `localhost:4566` and build and test against
AWS APIs on your laptop, with no account, no credentials, and no internet.

It is a community fork of the LocalStack community edition, which was archived
and put behind a mandatory account in March 2026. LocalEmu continues that
codebase under the Apache License 2.0, free and tokenless.

---

## Projects

| Project | Description |
|---|---|
| [localemu](https://github.com/localemu/localemu) | The AWS cloud emulator. 132 services, drop-in for the AWS CLI / boto3 / Terraform / CDK, Apache 2.0 |
| [localemu-examples](https://github.com/localemu/localemu-examples) | Runnable examples and quickstarts for common AWS workflows on LocalEmu |

---

## Quick start

```bash
pip install localemu[runtime]
localemu start -d

# real AWS CLI, pointed at localhost:4566, no account needed
awsemu s3 mb s3://my-bucket
awsemu dynamodb create-table --table-name Users \
  --attribute-definitions AttributeName=id,AttributeType=S \
  --key-schema AttributeName=id,KeyType=HASH \
  --billing-mode PAY_PER_REQUEST
```

---

## Why LocalEmu

- **Free and open.** Apache 2.0, no account, no auth token, no usage gates.
- **Drop-in.** Keep your existing code, Compose files, and CI. Change the
  endpoint, not your stack.
- **Real where it counts.** Lambda runs in the official AWS runtime images,
  RDS is a real PostgreSQL or MySQL, EC2 instances are real containers, and IAM
  policies actually deny when enforcement is on.
- **Community maintained.** Open contributions, public roadmap, responsive
  issues.

---

LocalEmu is an independent project and is not affiliated with, endorsed by, or
sponsored by LocalStack Inc. "LocalStack" is a trademark of its respective owner
and is used here only to describe the project's origin.
