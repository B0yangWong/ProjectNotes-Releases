# Changelog

## 0.6.2 — Formula dependency security update

- Updates KaTeX to 0.18.2, addressing the upstream low-severity [GHSA-238p-pmpm-9mq7](https://github.com/KaTeX/KaTeX/security/advisories/GHSA-238p-pmpm-9mq7). The advisory concerns inherited renderer options when another flaw has already polluted object prototypes; it is not a finding that ProjectNotes itself enables prototype pollution.
- Keeps explicit untrusted rendering and the editor’s no-network content policy. Adds regression checks for inherited trust settings, dangerous links, remote image directives, and normal fractions, roots, and matrices.
- Runtime dependency audit reports zero known advisories at the time of this build. This does not replace an independent security review.
- Rebuilds the Universal app; the editor layout, note format, library location, and green-yellow paper icon are unchanged.
- Supersedes the 0.6.1 preview. New downloads should use 0.6.2.

中文：升级公式组件至 0.18.2，修复上游低风险问题，并补充安全回归检查。构建时依赖检查未报告已知漏洞。界面、笔记格式和存储位置不变；下载请使用 0.6.2。

## 0.6.1 — First public Mac preview

- A standalone Universal app for Apple silicon and Intel, with the editor and required assets bundled.
- Project home, continue last edited, five recent notes, and per-note cursor/reading-position restoration.
- Rich text, selected-text sizing, formulas, tables, local image/PDF attachments, search highlights, and heading outline.
- Manual focus mode and layouts for smaller MacBook windows.
- Coalesced local saving with explicit save status and save-aware note switching and normal quit.
- Automatic local backup history and restore-as-new-copy recovery.
- Paginated A4 PDF export.
- English/Chinese interface and separate interface-size settings.
- Green-yellow black-hole accretion disk with a more visible paper design.

This is the first public download of this app. It is not Developer ID signed or notarized. Intel hardware, older macOS versions, and a separate clean-Mac first install remain untested.

## 中文

首个公开 Mac 预览版，提供独立通用应用下载。包含项目分类、最近编辑、位置恢复、富文本和公式、专注模式、小窗口布局、合并保存、自动备份与恢复、PDF 导出、中英文和界面字号设置。图标为黄绿色吸积盘与纸页设计。
