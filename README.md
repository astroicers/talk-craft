# talk-craft

簡報「怎麼寫」的 Claude Code skill——把專業簡報的**內容、敘事、邏輯**固化成跨工具規範，
讓第一版骨架就站得住論證。工具無關：與 `slidev-deck-stack`（怎麼用 Slidev 實作）疊用，
本 skill 管「寫什麼」，slidev 管「怎麼做」。

涵蓋方法論：Minto 金字塔原理 + SCQA + MECE、敘事弧（Sparkline / Hero / SCQA / Raskin 戰略
敘事 等）、ghost deck / dot-dash 骨架、Assertion-Evidence 投影片（句子標題 + 視覺證據，
Penn State 實證）、資料敘事（Knaflic 六堂課 + Tufte）、交付（throughline / STAR / 演練 /
demo 安全網）、依 talk 類型的框架選型、以及技術 / 實戰 demo talk 的 field-tested 實戰招式
（refrain / 進度地圖 / demo 當故事 / ATT&CK / kill-chain，含資安子節）。

## 結構

```
talk-craft/
├── README.md                   # 本文件
├── LICENSE                     # MIT
├── CHANGELOG.md                # 版本變更紀錄（Keep a Changelog + SemVer）
├── install.sh                  # 安裝腳本
├── .gitignore
├── .fact-check.md              # 簡報框架 / 來源查證紀錄（對照原典與權威來源）
├── .github/
│   └── workflows/
│       └── validate.yml        # CI：驗 JSON / SKILL frontmatter / 8 references 齊全
├── .claude-plugin/
│   ├── marketplace.json        # Claude Code Marketplace 定義
│   └── plugin.json             # Plugin 描述
└── skills/
    └── talk-craft/
        ├── SKILL.md            # 核心：五層架構 + 8 條鐵則 + 選型表 + 路由表
        └── references/         # 按需載入的完整方法論
            ├── narrative-arcs.md   # Minto 金字塔/SCQA/MECE、敘事弧 menu、ghost deck
            ├── slide-craft.md      # Assertion-Evidence、action title、訊噪比、認知負荷
            ├── data-viz.md         # Knaflic 六堂課、Tufte、圖表選型與誠信
            ├── delivery.md         # throughline、STAR、時間預算、演練、speaker notes、demo 安全網
            ├── talk-types.md       # talk 類型 → 框架對應（研究/顧問/pitch/keynote/數據）
            ├── anti-patterns.md    # 反模式對照表 + 上台前檢查清單
            ├── field-patterns.md   # 技術 / 實戰 demo talk 的 field-tested 實戰招式（含資安子節）
            └── sources.md          # 完整素材來源（書 / 學術 / web / GitHub skill / 公開講題）
```

## 安裝

> 以下方法**擇一**即可。全域安裝法（marketplace / install.sh / symlink / `npx skills -g`
> / `gh skill`）都會寫入 `~/.claude/skills/talk-craft`，**勿混用**以免版本不一致。

### 方法 A：Claude Code Marketplace（推薦）

1. Claude Code → **Manage Plugins** → **Marketplaces**
2. 貼上 `https://github.com/astroicers/talk-craft` → **Add**
3. 切到 **Plugins** tab，找到 `talk-craft` → **Install**

更新由 Claude Code 自行管理。

### 方法 B：安裝腳本

```bash
git clone https://github.com/astroicers/talk-craft.git
cd talk-craft
./install.sh          # 已存在會詢問；--force 直接覆蓋
```

### 方法 C：手動 symlink（開發本 skill 時，改 repo 即時生效）

```bash
# 先移除既有安裝（目錄或舊連結）——若目標已是目錄，ln 會把連結建到目錄「裡面」而非取代它
rm -rf ~/.claude/skills/talk-craft
ln -s "$(pwd)/skills/talk-craft" ~/.claude/skills/talk-craft
```

### 方法 D：npx skills / gh skill（跨 agent 開放安裝器）

open agent-skills 安裝器，Claude Code / Cursor / opencode 等通用（會自動偵測 agent）：

```bash
# 全域（user base，所有專案共用；知識層 skill 建議用這個）
npx skills add astroicers/talk-craft -g -a claude-code
# 僅本專案（裝到 ./.claude/skills/）
npx skills add astroicers/talk-craft -a claude-code
# 先預覽會裝哪些 skill（不安裝）
npx skills add astroicers/talk-craft --list
```

或用 GitHub CLI（gh v2.90+，GitHub 原生；預設目標是 Copilot，故需指定 agent）：

```bash
gh skill install astroicers/talk-craft --agent claude-code --scope user
```

驗證：

```bash
head -5 ~/.claude/skills/talk-craft/SKILL.md
```

## 更新

```bash
cd talk-craft
git pull
./install.sh --force
```

（symlink 安裝只需 `git pull`。）

## 解除安裝

```bash
rm -rf ~/.claude/skills/talk-craft
```

## 與 AI-SOP-Protocol（ASP）及其他 skill 搭配

本 skill 是**內容／溝通層**（簡報怎麼寫），ASP 是**治理層**（怎麼工作），兩者疊加、互不取代。

在做簡報的專案 CLAUDE.md 加入一行：

```
本專案簡報內容遵循 talk-craft skill，敘事與論證規範以該 skill 鐵則為準。
```

分工界線：

- 品質門檻（G1–G6）、commit 流程、ADR 紀律 → 聽 ASP。
- 與 `slidev-deck-stack` 互補疊加：**talk-craft 決定「寫什麼／怎麼組織論證」，slidev-deck-stack
  決定「怎麼用 Slidev 把它實作」**。兩者通常一起用：先用 talk-craft 把 governing thought、
  敘事骨架、每頁 action title 敲定，再交給 slidev-deck-stack 落成 deck。
- 與 `visual-web-stack` 並列：三者都是知識層 skill，各管一個領域（網頁技術棧 / Slidev 機制 /
  簡報內容），互不重疊。
- 衝突時：工作流程聽 ASP；簡報內容與論證聽本 skill；Slidev 實作細節聽 slidev-deck-stack。

## 素材來源對照表

撰寫基準：2026-06（查證紀錄見 `.fact-check.md`）。本 skill 的內容是公認簡報方法論的綜整，
**框架原典更新或本 skill 精煉時，更新對應的 references 檔並同步此表。**

| 方法論 / 框架 | 原始來源 | 對應 references 檔 |
|--------------|---------|--------------------|
| 金字塔原理 / SCQA / MECE | Barbara Minto《The Pyramid Principle》 | narrative-arcs.md |
| 敘事弧（Sparkline / what-is-what-could-be / STAR） | Nancy Duarte《Resonate》 | narrative-arcs.md、delivery.md |
| 戰略敘事（promised land / name the change） | Andy Raskin | narrative-arcs.md、talk-types.md |
| Assertion-Evidence（句子標題 + 視覺證據） | Michael Alley, Penn State《The Craft of Scientific Presentations》 | slide-craft.md |
| 極簡 / 訊噪比 / 圖優效應 | Garr Reynolds《Presentation Zen》 | slide-craft.md |
| 認知負荷 / 多媒體學習原則 | Mayer；Sweller | slide-craft.md |
| 資料敘事六堂課 / preattentive / Gestalt | Cole Nussbaumer Knaflic《Storytelling with Data》 | data-viz.md |
| data-ink / chartjunk / small multiples / sparkline | Edward Tufte | data-viz.md |
| throughline / 公開演講 | Chris Anderson《TED Talks》 | delivery.md |
| pitch 結構（10/20/30、10-slide） | Guy Kawasaki；Sequoia Capital | talk-types.md |

## License

MIT
