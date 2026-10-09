# 微豆投屏 WeDouCast — 版本发布仓库

局域网无线投屏（手机 → 电视/盒子），本仓库只存放**安装包与版本信息**，供已安装的 App 检查更新使用。

## 检查更新机制

- App 内：设置弹窗 →「检查更新」
- App 读取本仓库根目录的 `update.json`，与本地版本号比较
- 有新版本 → 提示更新说明 → 下载 APK（MD5 校验）→ 调起系统安装

## 发布流程（维护者）

1. 编译新版本 APK
2. 放入 `apk/`（文件名 `WeDouCast_v版本号.apk`，ASCII）
3. 更新根目录 `update.json`（versionCode 必须递增，md5 填新包校验值）
4. 推送到 main 分支

## 下载源

App 优先走 jsDelivr CDN（`cdn.jsdelivr.net/gh/zydzxymml/wedou-cast-release@main/...`），失败回落 `raw.githubusercontent.com`。

> 注意：jsDelivr 对分支文件有最长约 12 小时的 CDN 缓存，新版本发布后更新提示可能延迟数小时，属正常现象。
