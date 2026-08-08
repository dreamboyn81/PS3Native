# PS3Native APK 自动镜像

自动打包并转发 [maxjivi05/PS3Native](https://github.com/maxjivi05/PS3Native) 的最新 Android APK 构建产物到本仓库 Release。

> ⚠️ 本仓库不参与编译，只做「上游构建成功 → 下载 artifact → 发到本仓库 `latest` Release」的镜像中转。

## 下载最新 APK

进入 [Releases](https://github.com/dreamboyn81/PS3Native/releases) 页面，下载 **`latest`** 这个 Release 下的 `*.apk` 即可。
每次上游有新成功构建，会自动覆盖更新 `latest`，Release 标题带上游短 commit（如 `PS3Native 3c8604b`）。

## 自动更新机制

- 触发：GitHub Actions 定时 **每小时整点（UTC）** 检查一次 + 支持手动触发
- 逻辑：取上游 `android.yml` 最近一次 `success` run → 下载 artifact `ps3native-standard-debug` → 更新 `latest` Release
- 配置文件：`.github/workflows/apk.yml`

