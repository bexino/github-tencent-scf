# GitHub 部署腾讯云函数技能

将静态站点部署到腾讯云 SCF，使用 GitHub Actions 和腾讯云 Python SDK 更新函数代码，也支持迁移已有 Serverless 应用。

## 使用

e.g.

```text
请安装并使用使用 [github-tencent-scf](https://github.com/bexino/github-tencent-scf/) 技能，将本项目部署到腾讯云函数。
```

按提示登录腾讯云并提供站点名称。首次部署时，Agent 会协助创建函数和配置访问入口；迁移时会检查并沿用已有资源。

## GitHub 配置

在目标仓库的 **Settings → Secrets and variables → Actions** 中配置：

- **Secrets**：`TENCENT_SECRET_ID` 和 `TENCENT_SECRET_KEY`，分别填写腾讯云 SecretId 和 SecretKey。
- **Variables**：`SCF_FUNCTION_NAME`、`SCF_NAMESPACE` 和 `SCF_REGION`，填写实际函数名、命名空间和地域。

不要在聊天或公开仓库中提供密钥。技能说明见 [SKILL.md](SKILL.md)，`assets/` 包含需要根据目标项目调整的示例。

## 许可证

AGPL-3.0