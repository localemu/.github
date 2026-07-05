<p align="center">
  <img src="https://raw.githubusercontent.com/localemu/.github/main/profile/assets/localemu-logo.png" alt="LocalEmu logo" width="110" />
</p>

<h1 align="center">LocalEmu</h1>

<p align="center"><b>Run AWS locally. No account. No token. No sign-up.</b></p>

<p align="center">
Free, open-source AWS cloud emulator. Point the AWS CLI, boto3, Terraform, or CDK<br/>
you already use at <code>localhost:4566</code> and build against AWS APIs on your laptop.
</p>

<p align="center">
  <a href="#quick-start"><img src="https://img.shields.io/badge/🚀_Quick_Start-0894ab?style=for-the-badge&logoColor=white" alt="Quick Start" /></a>
  <a href="https://github.com/localemu/localemu"><img src="https://img.shields.io/badge/Emulator-181717?style=for-the-badge&logo=github&logoColor=white" alt="Emulator repo" /></a>
  <a href="https://github.com/localemu/localemu-examples"><img src="https://img.shields.io/badge/Examples-38bdf8?style=for-the-badge&logoColor=white" alt="Examples" /></a>
</p>

<p align="center">
  <b><a href="https://github.com/localemu/localemu">LocalEmu Emulator</a></b> |
  <b><a href="https://github.com/localemu/localemu-examples">Examples & Quickstarts</a></b> |
  <b><a href="https://tocconsulting.fr">TocConsulting</a></b>
</p>

<p align="center">
  <a href="https://pypi.org/project/localemu/"><img src="https://img.shields.io/pypi/v/localemu?color=0894ab" alt="PyPI" /></a>
  <a href="https://github.com/localemu/localemu/stargazers"><img src="https://img.shields.io/github/stars/localemu/localemu?style=flat&color=38bdf8" alt="GitHub stars" /></a>
  <a href="https://github.com/localemu/localemu/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-Apache%202.0-blue" alt="License" /></a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/localemu/.github/main/profile/assets/localemu-in-action.png" alt="LocalEmu in action: your AWS CLI, Terraform, and boto3 talk to localhost:4566, which emulates 132 AWS services on your laptop" width="100%" />
</p>

LocalEmu is a community fork of the LocalStack community edition, which was
archived and put behind a mandatory account in March 2026. LocalEmu continues
that codebase under the Apache License 2.0, free and tokenless.

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

Maintained by [TocConsulting](https://tocconsulting.fr), together with the community.

LocalEmu is an independent project and is not affiliated with, endorsed by, or
sponsored by LocalStack Inc. "LocalStack" is a trademark of its respective owner
and is used here only to describe the project's origin.
