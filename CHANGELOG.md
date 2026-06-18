# Changelog

本專案的所有重大變更記錄於此。格式依循 [Keep a Changelog](https://keepachangelog.com/zh-TW/1.1.0/)，版本遵循 [Semantic Versioning](https://semver.org/lang/zh-TW/)。

## [1.0.0] - 2026-06-18

首個正式版。專業簡報撰寫（內容/敘事/邏輯）的 Claude Code skill / plugin，工具無關。

### Added

- 五層架構（訊息 / 結構 / 投影片 / 證據 / 交付）+ 8 條鐵則的 `SKILL.md` 核心規範，
  含「敘事與框架選型表」與「references 路由表」，並標明判斷題守則與鐵則的界線。
- 7 份 references 方法論：`narrative-arcs`（Minto 金字塔/SCQA/MECE、敘事弧 menu、ghost deck/dot-dash、
  Duarte Sparkline、Raskin 戰略敘事）、`slide-craft`（Assertion-Evidence、action title、訊噪比、認知負荷）、
  `data-viz`（Knaflic 六堂課、Tufte、圖表誠信）、`delivery`（throughline、STAR、演練、speaker notes、
  demo 安全網）、`talk-types`（類型→框架，含 pitch 細節）、`anti-patterns`（反模式對照表 + 上台前檢查清單）、
  `sources`（完整素材來源與授權）。
- Claude Code marketplace 支援：`.claude-plugin/marketplace.json` + `plugin.json`，可從 Manage Plugins →
  Marketplaces 加入安裝；README 含 marketplace / install.sh / symlink / `npx skills` / `gh skill` 四種安裝法。
- `install.sh` 安裝腳本（POSIX 相容、`--force`）與 CI `validate.yml`（驗 JSON / SKILL frontmatter / 7 references）。
- `.fact-check.md` 簡報框架查證紀錄（對照 Minto / Alley / Duarte / Knaflic / Kawasaki 等原典與權威來源）。

### Notes

- 與 `slidev-deck-stack` 互補：talk-craft 管「寫什麼」，slidev-deck-stack 管「怎麼用 Slidev 實作」；
  與 `visual-web-stack` 並列為知識層 skill。三者同模、各管一個領域。

[1.0.0]: https://github.com/astroicers/talk-craft/releases/tag/v1.0.0
