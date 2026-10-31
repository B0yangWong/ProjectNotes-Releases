# Validation Scope / 验证范围

This preview has been checked on the development Apple silicon Mac running macOS 27.2. A successful build is not a claim that every supported Mac or first-download security flow has been tested.

## Checks for This Public Download

- Optimized Universal build with native `arm64` and `x86_64` slices. Both executable slices have a macOS 14.0 minimum target.
- The app includes its editor, styles, fonts, formula renderer, icon resources, and license notices. Required libraries are system libraries; no Xcode directory is used as a runtime search path.
- Local ad-hoc signature and hardened runtime checked. The ZIP was extracted again and the extracted app's signature verified. Files in the ZIP match the audited app. There is no Developer ID identity or notarization; local Gatekeeper assessment rejects this unnotarized preview, so a clean download may be blocked.
- The extracted app opened with a new, isolated, empty library. A project and a note were created through the actual interface; English, Chinese, and a slash-fraction formula were entered, saved, quit normally, and reopened.
- A final automatic backup contained the latest invented note and formula. The existing personal library was not used in testing and its records and attachment files remained unchanged.
- Actual English/Chinese interfaces, project home, rich-text formula/table display, and focus-mode entry/exit were inspected using synthetic data. Public screenshots contain only the app window and invented content; macOS's capture indicator can appear in the title bar.
- A one-page A4 PDF was exported from the extracted app. Its title, English/Chinese text, and formula rendered correctly with macOS PDFKit, without toolbars or save status. See the text-copying limit below.
- A file allowlist excludes source, databases, note/attachment stores, backups, test output, environment files, and development metadata. Pattern scans checked the bundle and public files for local home paths, known personal identifiers, and common secret formats. Public images were visually inspected and have no GPS or camera-owner tags. These checks reduce accidental disclosure; they are not an independent security audit.
- Third-party license texts for 49 editor runtime packages are bundled and published. The release provides a SHA-256 checksum; it checks file agreement, not publisher identity or safety.

## Remaining Limits

- Intel hardware, older macOS versions, and first installation on a separate clean Mac have not been tested. The build target and included architecture are not substitutes for those tests.
- PDF text copying/extraction varies by reader. macOS PDFKit extracted Chinese and English but collapsed a repeated letter in one word; the bundled third-party extraction/rendering tools also had font-mapping compatibility problems with this macOS-generated PDF. Native visual rendering was correct. Verify copied PDF text, especially for important work; broad cross-reader PDF compatibility is not certified.
- This public-packaging pass did not repeat every prior long-document, input-method, disk-full, backup-retention, attachment-recovery, or multi-page printing test. It does not establish a speed guarantee or cover every failure mode.
- Notes and backups are not independently encrypted. Local backups on the same disk cannot protect against losing the disk. Save/backup failures and force quitting can still lose pending changes.
- No iCloud, iPhone app, collaboration, Apple Notes import, OCR, PDF annotation, or automatic updater is included.

## 中文摘要

本次在开发用 Apple 芯片 Mac 上检查了通用包构建、两种架构的最低系统目标、签名、解压后首次启动、新建、中英文与公式保存、退出后最新备份、重开、专注模式，以及一页 A4 PDF 的原生显示。正式资料库保持原样。下载包和公开页面已做文件范围与隐私特征检查，截图使用虚构资料。

Intel 真机、旧系统、另一台全新 Mac 的安全提示和全部历史回归用例没有在本轮重新实测。PDF 的不同阅读器存在文字提取差异，原生显示正常，但复制结果应自行核对。本版没有 Apple 开发者身份签名或公证，也不等于经过独立安全审计。
