# Install ProjectNotes / 安装项目笔记

## Compatibility

- Download: `ProjectNotes-0.6.2-macOS-universal.zip`.
- Includes native `arm64` and `x86_64` executables for Apple silicon and Intel Macs.
- Both executable slices have a macOS 14.0 minimum deployment target. This is a build target, not a claim of testing every supported OS.
- Checked on the development Apple silicon Mac. Intel hardware, older macOS, and a separate clean Mac have not been tested.
- The editor, fonts, formula renderer, and third-party notices are bundled. No Xcode, Node.js, app account, network server, or package-manager installation is needed.
- This preview is ad-hoc signed with hardened runtime; it has no Developer ID identity or Apple notarization.

## Install and First Launch

1. Download the app ZIP from [v0.6.2](https://github.com/B0yangWong/ProjectNotes-Releases/releases/tag/v0.6.2). The “Source code” assets are documentation archives, not app installers.
2. Extract and move `ProjectNotes.app` into Applications. Do not run it from inside the archive. Keep the accompanying notices available in the app's Resources folder.
3. Open the app. If macOS cannot verify the developer, only proceed if you trust this release. After the first attempt, follow [Apple's manual instructions](https://support.apple.com/en-us/102445) under System Settings → Privacy & Security → Open Anyway, if available. Managed Macs may forbid this. Do not disable Gatekeeper globally or use a script to remove download quarantine.
4. A warning that the app is damaged or will harm your computer is a reason to stop and report the problem, not an instruction to bypass it.
5. Create a project, then a note. To change Chinese to English, choose 设置 → 语言 → English.

The app does not install a background agent, request Accessibility or Screen Recording access, or start at login. File dialogs are used when you import, export, or choose a backup directory.

## Check the Download

Download `SHA256SUMS.txt` from the same release. In Terminal, change to the download folder and run:

```sh
shasum -a 256 ProjectNotes-0.6.2-macOS-universal.zip
```

Compare the result with the ZIP's entry in `SHA256SUMS.txt`. This detects disagreement with the published file; it is not a digital signature, security audit, or Apple approval.

## Updates and Existing Data

Export a library backup before updating, quit the older app normally, then replace it. Leave `~/Library/Application Support/ProjectNotes/` intact. Settings for this public app use the identifier `app.projectnotes.mac`; settings from an earlier private development build may need to be selected again. The library folder stays the same. Do not run two development/public copies against the same library at once.

If saving fails, keep the app open and resolve the error. Force quitting does not wait for pending content or the final automatic backup. Automatic backups on the same disk are not protection against disk loss; Settings lets you choose another disk.

## 中文安装要点

下载带有 `macOS-universal.zip` 的应用压缩包，解压后拖入“应用程序”。安装包包含 Apple 芯片和 Intel 架构，最低构建目标为 macOS 14，但 Intel 真机、旧系统和另一台全新 Mac 尚未实测。

本版没有 Apple 开发者身份签名和公证，首次启动可能被拦截。确认信任下载后，仅按 [Apple 官方说明](https://support.apple.com/zh-cn/102445)手动允许；不要关闭系统安全检查、运行移除隔离标记的脚本，或绕过“将损害电脑”“已损坏”提示。

更新前先导出备份并正常退出，再替换应用，保留原来的资料库目录。公开版使用独立的应用标识，早期开发版的界面设置可能需要重选，笔记目录不变。不要让两个应用副本同时操作同一资料库。
