okteto-infra
---

**[简体中文](./README.md)** | [English](./README_en-US.md)

> 一个C#程序，用于在AWS上部署Kubernetes集群（可能是okteto环境）。

![](https://www.pulumi.com/templates/kubernetes/aws/architecture.png)

## Pulumi Cloud

- [okteto-infra/main](https://app.pulumi.com/Jeff-Tian/okteto-infra/main)

## 使用到的技术

- AWS Cloud (cli)
- dotnet (C#)
- Pulumi (cli and nuget)

## 前置条件

安装 Pulumi Cli 和 AWS Cli

- [Pulumi CLI](https://www.pulumi.com/docs/get-started/install/)
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)

```
➜  okteto-infra git:(main) ✗ aws --version
aws-cli/2.9.4 Python/3.11.0 Darwin/23.2.0 source/x86_64 prompt/off
➜  okteto-infra git:(main) ✗ pulumi version
v3.95.0
```

## CI/CD

使用 GitHub Actions 来部署基础设施的变化到不同的环境，这里用到了：

- `aws-actions/configure-aws-credentials` - 确定用来部署到 AWS 账号所需要的角色
- `pulumi/actions` - 通过 Pulumi 将栈部署到 AWS 账号


