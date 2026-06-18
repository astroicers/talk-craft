# Changelog

本專案的所有重大變更記錄於此。格式依循 [Keep a Changelog](https://keepachangelog.com/zh-TW/1.1.0/)，版本遵循 [Semantic Versioning](https://semver.org/lang/zh-TW/)。

## [1.2.0] - 2026-06-18

### Added

- `references/templates.md`：可複製填空骨架——SCQA 執行摘要、Knaflic Big Idea worksheet、
  **ghost-deck 交棒物**（與 slidev-deck-stack 的共用契約：deck header + 每頁 `slide` 區塊
  title/assertion/exhibit/reveal/note）。
- `references/worked-example.md`：從主題到 ghost-deck 的端到端走查示範（不附成品 deck）。

### Changed

- `SKILL.md`：在「與 slidev-deck-stack 互補」寫死 ghost-deck 交棒契約與職責切點
  （design-direction／雙語內容歸 talk-craft；theme／font 歸 slidev）；references 路由表加
  templates / worked-example 兩列；triggers 補 keynote / data viz / throughline / STAR /
  Minto / Duarte / Knaflic；anti-patterns checklist 標為寫後驗收 gate。
- `slide-craft.md`：句子標題規格拆中英雙版（英文 8–14 words；中文約 15–25 字）；
  「統計顯著」措辭改引原典 p<.01。
- `.fact-check.md` #3：改引 Garner & Alley (2013) 原典並註明 WUSTL 為二手摘要；#2 移除幽靈
  `~28pt` 規格。
- `field-patterns.md`：去兩處越界絕對化措辭（「最強單一技巧」→「最有效之一」；ATT&CK
  「天然 MECE」→「近似 MECE」）。
- `README.md` 結構樹／CI 註解、`validate.yml`（references 8 → 10）同步。

## [1.1.0] - 2026-06-18

### Added

- `references/field-patterns.md`：技術 / 實戰 demo talk 的 field-tested 實戰招式——refrain 鼓點、
  累積式進度地圖、demo 當故事（setup→tension→reveal→payoff）、延伸類比、抽象↔具體對照表、
  賭注接地、戰果計分板、競品定位表、鏡像結構，外加資安 / 紅隊 / 雲端子節（ATT&CK 骨架、
  kill-chain 敘事弧、live exploit 安全網 + OPSEC、免責頁），並附公開講題範例研究清單。
- 招式來自實際交付的 conference talk 與公認優秀講題（DEF CON / Black Hat best-of、SANS SEC403 等）
  萃取，於 `sources.md` / `.fact-check.md` 標明為 practitioner 模式、非書本原典。

### Changed

- `SKILL.md` 選型表與 references 路由表新增「技術 demo / 實戰 walkthrough / 資安攻防」一列，
  description / triggers 補實戰 demo 相關詞。
- `delivery.md` 補 hook 具體可仿例與「受眾自評三問」CTA 變體、demo-as-story 交叉連結；
  `talk-types.md` 新增實戰 demo 列；`narrative-arcs.md` 弧 menu 新增「旅程 / 走查弧（kill-chain）」。
- `README.md` 結構樹與方法論說明、CI `validate.yml`（references 7 → 8）同步更新。

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
