# Privacy / 隐私说明

ProjectNotes works locally. It has no app account, advertising, analytics upload, cloud sync, or automatic update service. GitHub hosts downloads and public feedback; the app does not send your library to GitHub.

## Local Records

The default library is `~/Library/Application Support/ProjectNotes/`:

- `Library.store` and related database files store projects, rich-text note content, timestamps, revisions, and Recently Deleted records.
- `Attachments/` stores copied images and PDF attachments, including filenames. Some imported image formats are converted for display.
- `WorkspaceState.json` stores recently opened notes, selections, and reading positions.
- `AutomaticBackups/` is the default automatic-backup location. Backups include note contents and attachments, including content that may since have been edited or deleted. Settings can choose a different directory or disk.

Language, interface size, text preferences, and backup preferences use macOS preferences under `app.projectnotes.mac`. The editor uses a nonpersistent WebKit data store; its scripts, styles, fonts, and formula renderer are bundled locally. These records and backups are not independently encrypted by ProjectNotes. macOS FileVault, Time Machine, cloud-synced folders, system diagnostics, and disk permissions are separate from the app.

## Actions You Control

You select files for importing attachments, exporting PDFs, exporting/importing backups, and choosing a backup location. Clicking an external HTTP or HTTPS link hands it to your default browser; that site and your browser then handle the request. Previewing attachments opens a local viewer. Clipboard operations use the system clipboard when you copy or paste. Other applications and system services have their own privacy behavior.

Local automatic backups are enabled by default, created initially and after changes every 15 minutes, and supplemented on normal quit. The latest 20 are retained after a successful new backup. An error can prevent a new backup or cleanup. Moving backups to a folder managed by a cloud provider or another disk makes that provider/disk part of your storage arrangement; ProjectNotes does not add a cloud service itself.

## Removal and Recovery

Recently Deleted is recoverable storage, not secure erasure. Restoring from a backup creates a new copy. Uninstalling the app does not remove its library, backups, chosen external backup directories, exported files, or OS backups.

To remove local records, quit the app normally, then remove the library folder and any separately chosen backup/export copies you no longer need. Preferences can be removed separately. Consider whether macOS or another backup service still retains copies. Do not delete a library while the app is running. If you need to retain data, export a backup first.

## Public Feedback

GitHub issues and attachments can be public. Use invented notes and redact usernames, paths, names, email addresses, and confidential material from screenshots. Do not upload a real library or backup. See [Security](SECURITY.md) for vulnerability reporting.

## 中文摘要

应用将笔记、附件、阅读位置和备份保存在本机，不自动上传到 GitHub，没有账户、广告、统计上传、云同步或自动更新检查。默认备份可能保留已经修改或删除的旧内容；应用不单独加密这些文件。

点击外部链接才交给浏览器，导入、导出和复制粘贴均由用户操作触发。若你选择云盘中的备份目录，云盘服务可能同步这些文件；系统备份与磁盘加密由 macOS 单独管理。

卸载应用不会删除资料库和备份。“最近删除”不是安全擦除。需要清除资料时，先正常退出，再处理资料库、外部备份、导出副本及其他备份服务中的副本。公开反馈使用虚构内容，不要上传私人笔记或真实备份。
