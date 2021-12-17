# devops-rn-app

[![Android](https://github.com/RootLinkFE/devops-rn-app/actions/workflows/manually-build-android.yml/badge.svg)](https://github.com/RootLinkFE/devops-rn-app/actions/workflows/manually-build-android.yml)
[![IOS](https://github.com/RootLinkFE/devops-rn-app/actions/workflows/manually-build-ios.yml/badge.svg)](https://github.com/RootLinkFE/devops-app/actions/workflows/manually-build-ios.yml)

利用 Action 构建私库 gitlab rn app 代码

- 支持 Android
- 支持 IOS

## 使用

- 1、通过模板的方式引用此模板创建工程
- 2、配置 Secret

```yaml
env:
  GITLAB_REPO_URL: ${{ secrets.GITLAB_REPO_URL }}
  WECOM_WEBHOOK_KEY: ${{ secrets.WECOM_WEBHOOK_KEY }}
  MENTION_MOBILE_LIST: ${{ secrets.MENTION_MOBILE_LIST }}
```

另外还有蒲公英 `PGYER_API_KEY` Secret

## 其他

实现总结文章：[GitHub Actions 实现 RN App 自动化构建并推送到蒲公英](https://github.com/giscafer/blog/issues/53)
