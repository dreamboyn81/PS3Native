# PS3Native APK 自动镜像

[PS3Native](https://github.com/maxjivi05/PS3Native) 是基于 [RPCS3](https://github.com/RPCS3/rpcs3) 的 **PlayStation 3 emulator and debugger / PlayStation 3 模拟器与调试器** 的 Android 移植分支。

上游原仓库描述为：

> PlayStation 3 emulator and debugger

相关链接：

- 上游仓库：https://github.com/maxjivi05/PS3Native
- RPCS3 原项目：https://github.com/RPCS3/rpcs3
- 官方网站：https://rpcs3.net/
- 上游更新日志：https://github.com/maxjivi05/PS3Native/commits?author=maxjivi05

本仓库 **不开发模拟器本体**，也不参与编译源码，只自动从上游拉取最新成功构建的 Android APK，并发布/更新到本仓库的 `latest` Release，方便直接下载安装。

## 下载最新 APK

前往 [Releases](https://github.com/dreamboyn81/PS3Native/releases) 页面，下载 `latest` Release 中的 `*.apk` 文件即可。

每次上游有新成功构建时，`latest` Release 会自动更新，并附带最近提交记录和完整更新日志链接。

## 自动更新机制

- 触发方式：GitHub Actions 每小时检查一次，也支持手动触发
- 工作流程：检查上游 `android.yml` 最近一次成功构建 → 下载 APK Artifact → 发布/覆盖 `latest` Release
- 配置文件：`.github/workflows/apk.yml`

## 发布页内容

每次发布的 `latest` Release 会包含：

- 对应上游 Actions Run 链接
- 当前上游短 commit SHA
- 最近几次上游提交摘要
- 完整更新日志链接：  
  https://github.com/maxjivi05/PS3Native/commits?author=maxjivi05

## 授权与声明

上游项目及本镜像分发均遵循原项目授权。

- 上游 License：GNU General Public License v2.0
- 模拟器代码、构建产物与版权归属均来自上游 [maxjivi05/PS3Native](https://github.com/maxjivi05/PS3Native) / [RPCS3/rpcs3](https://github.com/RPCS3/rpcs3)
- 本仓库仅做 APK 镜像与分发，不声称拥有模拟器本体的开发版权

## 温馨提示

PS3 模拟器仅可用于运行您合法拥有并备份的游戏或自制程序。请遵守当地法律法规及游戏版权相关协议。
