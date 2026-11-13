# GitHub 部署腾讯云函数技能

将静态站点部署到腾讯云 SCF，使用 GitHub Actions 和腾讯云 Python SDK 更新函数代码，也支持迁移已有 Serverless 应用。

## 使用

e.g.

```text
请安装并使用使用 [github-tencent-scf](https://github.com/bexino/github-tencent-scf/) 技能，将本项目部署到腾讯云函数。
```

按提示登录腾讯云。Agent 会核实站点及资源归属、配置访问入口；新网站默认创建独立函数，迁移时仅沿用确认属于该网站的现有函数。

## GitHub 配置

在目标仓库的 **Settings → Secrets and variables → Actions** 中配置：

- **Secrets**：示例工作流需要 `TENCENT_SECRET_ID` 和 `TENCENT_SECRET_KEY`，分别为腾讯云 SecretId 和 SecretKey；已有可用配置可以继续使用。
- **Variables**：`SCF_FUNCTION_NAME`、`SCF_NAMESPACE` 和 `SCF_REGION` 分别为实际函数名、命名空间和地域，Agent 会在有权限时配置并核对。用户未指定地域且没有明确的既有部署目标时，默认使用上海（`ap-shanghai`）；已有目标使用其实际地域。

不要在聊天或公开仓库中提供密钥。技能说明见 [SKILL.md](SKILL.md)，`assets/` 包含需要根据目标项目调整的示例。

## 许可证

AGPL-3.0
