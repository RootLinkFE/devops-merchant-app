# devops-merchant-app

[![Android](https://github.com/RootLinkFE/devops-merchant-app/actions/workflows/manually-build-android.yml/badge.svg)](https://github.com/RootLinkFE/devops-merchant-app/actions/workflows/manually-build-android.yml)
[![IOS](https://github.com/RootLinkFE/devops-merchant-app/actions/workflows/manually-build-ios.yml/badge.svg)](https://github.com/RootLinkFE/devops-merchant-app/actions/workflows/manually-build-ios.yml)

利用 Action 构建私库 gitlab rn app 代码

- 支持 Android
- 支持 IOS

## 使用

- 1、通过模板的方式引用此模板创建工程
- 2、配置 Secret

```yaml
env:
  GITLAB_REPO_URL: ${{ secrets.GITLAB_REPO_URL }} # 仓库oauth2 地址
  WECOM_WEBHOOK_KEY: ${{ secrets.WECOM_WEBHOOK_KEY }} # 企业微信 webhook key
  MENTION_MOBILE_LIST: ${{ secrets.MENTION_MOBILE_LIST }} # 企业微信@人员手机号（可不填）
```

- `PGYER_API_KEY` 蒲公英 api 上传 key
- `CODE_SIGNING_IDENTITY` IOS code-signing-identity
- `TEAM_ID` IOS 证书 TEAM ID

IOS:

代码文件下放对应证书 `p12` 和 `mobileprovision`

```yaml
with:
  project-path: ios/app.xcodeproj
  workspace-path: ios/app.xcworkspace
  p12-path: ios/app.p12
  mobileprovision-path: ios/app.mobileprovision
```

## 其他

实现总结文章：[GitHub Actions 实现 RN App 自动化构建并推送到蒲公英](https://github.com/giscafer/blog/issues/53)
