# Caravel Releases

这里仅存放 Caravel 桌面应用的公开安装包和 Tauri 自动更新文件，源代码仍在私有仓库中维护。

macOS 开发者内测包暂未使用 Apple Developer ID 签名或公证。首次安装后，如系统阻止打开，请执行：

```bash
sudo xattr -cr "/Applications/Caravel.app"
```

应用内自动更新会额外校验 Tauri 更新签名；签名私钥仅保存在 GitHub Actions Secrets 中。
