# Fork 声明 / Fork Notice

本仓库是 [op7418/guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill) 的独立分支（AGPL-3.0）。

| 项目 | 内容 |
|------|------|
| 上游仓库 | https://github.com/op7418/guizang-ppt-skill |
| 分叉基点 | 上游 commit `c91369c449d34755d320a8b81d0734000d99d1ab`（"add presenter view preview to readme"） |
| 上游作者 | [歸藏 (op7418)](https://github.com/op7418) |
| 上游许可证 | AGPL-3.0（见 `LICENSE`，保持不变） |
| 本仓库 | https://github.com/Rococo0614/ppt_skill_local |
| 本仓库维护者 | [Rococo0614](https://github.com/Rococo0614) |

## 本分支的修改

在原版 Style A（电子杂志 × 电子墨水）与 Style B（瑞士国际主义）之上新增 **Style C · 清华大学风**：

| 文件 | 变更 |
|------|------|
| `assets/template-tsinghua.html` | 新增：从 `template-swiss.html` 派生，锚点色换为清华紫 `#660874`，低功耗事件名改为 `tsinghua-low-power-change`，WebGL 兜底 hex 同步 |
| `references/themes-tsinghua.md` | 新增：4 套清华紫主题色预设（清华紫 / 深紫菫 / 丁香紫 / 紫灰学术） |
| `references/layouts-tsinghua.md` | 新增：Style C 版式说明（转发自 `layouts-swiss.md` + 差异清单） |
| `SKILL.md` | 修改：新增风格 C 章节、7 问清单、主题色表、必查项、资源导览与加载顺序 |
| `README.md` / `README.en.md` | 修改：三视觉系统说明、Style C 主题表、安装命令指向本仓库、License 行、移除上游赞助 badge |
| `scripts/check-presenter-runtime-sync.mjs` | 修改：演讲者运行时防漂移检查纳入第三份模板 |

上游其余文件（模板、校验器、演讲者模式、版式锁等）均未改动。

## 许可证

本项目整体继承上游的 **AGPL-3.0** 许可（`LICENSE` 文件保持原样）。本分支新增与修改的部分同样以 AGPL-3.0 发布。

AGPL-3.0 © 2026 [op7418](https://github.com/op7418) · 本分支修改 © 2026 [Rococo0614](https://github.com/Rococo0614)

## 赞助说明

上游的赞助方（360 安全龙虾、Kimi work、Cola Skill、真格 Token Grant）仅支持原项目 `op7418/guizang-ppt-skill`，本分支不继承、不代表任何赞助关系。相关赞助信息见上游 [SPONSORS.md](https://github.com/op7418/guizang-ppt-skill/blob/main/SPONSORS.md)。

## 与上游同步

本仓库已移除上游 `.git` 历史（独立 git 仓库）。如需同步上游后续更新，建议按补丁方式手动合并：`git fetch https://github.com/op7418/guizang-ppt-skill.git main` 后对新增/变更文件逐个 diff，特别关注 `SKILL.md` 与 `assets/template-*.html`（清华模板与 swiss 模板的演讲者运行时区块需要保持同步，可运行 `node scripts/check-presenter-runtime-sync.mjs` 验证）。
