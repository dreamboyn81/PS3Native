# PS3Native APK 自动镜像

自动从 [maxjivi05/PS3Native](https://github.com/maxjivi05/PS3Native) 拉取最新的 Android APK 构建产物，并发布到本仓库的 Release 中。

## 工作原理

- 每小时自动检查上游仓库的最新成功构建
- 下载对应的 APK artifact（`ps3native-standard-debug`）
- 发布/更新到本仓库的 `latest` Release 标签下
- 也支持手动触发（Actions → Run workflow）

## 使用方式

### 下载最新 APK

1. 进入本仓库的 [Releases](https://github.com/dreamboyn81/PS3Native/releases) 页面
2. 找到名为 **latest** 的 Release
3. 下载里面的 `.apk` 文件即可

### 手动触发构建

1. 进入 **Actions** 标签页
2. 左侧选择 **"自动镜像 PS3Native APK"**
3. 点击 **Run workflow** → 绿色按钮确认

## 注意事项

- 本仓库仅作镜像转发，不修改上游代码
- 上游仓库：[maxjivi05/PS3Native](https://github.com/maxjivi05/PS3Native)
- 如有问题请优先在上游仓库反馈
