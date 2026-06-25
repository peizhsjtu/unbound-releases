# unbound-releases

逍遥游 Unbound App 的 OTA 分发仓库（Public）。

## 文件结构

- `manifest.json` — App 检查更新的元数据
- Release Assets — 各版本的 APK 文件

## App 端配置

UpdateService 的 `defaultManifestUrl` 指向本仓库的 raw `manifest.json`。

## 发布新版本流程

1. 在代码仓库构建 release APK：`flutter build apk --release`
2. 复制 APK 到本地 clone 的 unbound-releases 仓库
3. 更新 manifest.json 的 version/versionCode/url/changelog
4. push 到 main
5. 在 GitHub 网页创建 Release + 上传 APK 作为 asset
