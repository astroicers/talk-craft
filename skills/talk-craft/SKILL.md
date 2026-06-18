---
name: talk-craft
description: |
  專業簡報撰寫規範（工具無關，管「寫什麼」不管「用什麼工具做」），涵蓋 Minto 金字塔/SCQA/MECE
  + 敘事弧（Sparkline / Hero / SCQA / Raskin）+ ghost deck/dot-dash 骨架 + Assertion-Evidence
  投影片（句子標題 + 視覺證據）+ action title + 訊噪比與認知負荷 + 資料敘事（Knaflic/Tufte）
  + 交付（throughline / STAR / 演練 / demo 安全網）+ 依 talk 類型選框架
  + 技術 / 實戰 demo talk 的 field-tested 實戰招式（refrain / 進度地圖 / demo 當故事 / kill-chain / ATT&CK 骨架）。
  當你要寫、規劃或改一份簡報、研討會 talk、pitch、技術分享、述職的「內容與論證」時必須載入——
  與做投影片的工具無關，先把內容想清楚再開 Slidev/PPT。
  Handles: 定 governing thought、選敘事弧、排 ghost deck、下 action title、每頁 assertion-evidence、
  圖表敘事、講者交付與演練、依類型選框架。
  Triggers: 簡報, 投影片, slides, deck, talk, pitch, 路演, 研討會, 技術分享, 述職, 匯報,
  怎麼寫簡報, 簡報結構, 敘事, storytelling, 金字塔原理, pyramid, SCQA, assertion-evidence,
  action title, ghost deck, 開場, 結尾, 上台, 演練, 實戰 demo, walkthrough, 攻防展示, kill chain, ATT&CK, 資安 talk,
  keynote, 演講, 簡報技巧, 資料視覺化, 圖表, data viz, storytelling with data, throughline, STAR, Minto, Duarte, Knaflic.
---

# Talk Craft — 專業簡報撰寫規範

本 skill 固化「把簡報內容寫對」（研討會 talk、pitch、技術分享、商業匯報、述職）的方法論。
目標：**第一版骨架就站得住論證**，不靠事後重排補課。工具無關——管「寫什麼/怎麼組織論證」，
不管「用什麼工具做」；與 `slidev-deck-stack`（怎麼用 Slidev 實作）互補疊用。

撰寫基準：2026-06。內容是公認簡報方法論（Minto、Alley assertion-evidence、Duarte、Knaflic、
Kawasaki/Sequoia、TED 等）的綜整，框架原典與查證紀錄見 repo 根目錄 `.fact-check.md`、`sources.md`。

## 五層架構

```
┌──────────────────────────────────────────────────────────────┐
│  訊息層（Message）                                            │
│  governing thought / big idea ── 一句話講不出來就還沒成形      │
├──────────────────────────────────────────────────────────────┤
│  結構層（Structure）                                          │
│  金字塔（answer-first）＋ SCQA 開場 ＋ MECE 分組               │
│  ＋ 敘事弧選型 ＋ ghost deck / dot-dash 骨架                   │
├──────────────────────────────────────────────────────────────┤
│  投影片層（Slide）                                            │
│  Assertion-Evidence：句子標題（論點）＋ 視覺證據（非 bullet）  │
│  ＋ 一頁一想法 ＋ 訊噪比 ＋ 認知負荷                           │
├──────────────────────────────────────────────────────────────┤
│  證據層（Data & Evidence）                                    │
│  Knaflic 六堂課 ＋ Tufte ── 在圖上直接點出 takeaway           │
├──────────────────────────────────────────────────────────────┤
│  交付層（Delivery）                                           │
│  throughline ＋ 60 秒 hook ＋ STAR ＋ 演練 ＋ demo 安全網      │
│  ＋ 結尾 CTA（recency）                                        │
└──────────────────────────────────────────────────────────────┘
```

**核心原則**：先有單一訊息（governing thought），才有結構（敘事弧 + 金字塔），才有投影片
（assertion-evidence）；**內容定稿才碰視覺**；標題下論點、不下主題。

## 鐵則（MUST，違反即重寫）

1. **一份簡報只有一個 governing thought** 整場回答一個問題，核心是單一論點（answer，不是主題）。
   一句話講不出來，就是還沒想清楚——先別做頁。（Minto「big idea」/ Duarte）
2. **結論先行（answer-first）** 第一頁／執行摘要就講答案，再用論證支撐；不要鋪陳到最後才揭曉。
   受眾隨時可能離席、分心或時間被砍，最關鍵的東西放最後等於沒講到。（Minto / Kawasaki）
3. **每頁標題是完整論點句，不是主題標籤** 「市場成長但破碎且競爭激烈」而非「市場分析」
   （action title / assertion headline）。把所有標題單獨讀完，應等於整份論證。
4. **Ghost deck 先過，才做頁** 先把每頁 action title 列成骨架，串起來讀必須像連貫段落；
   讀不通先重排結構，**不要先做幾十頁再砍**。改結構便宜，改頁貴（先拿骨架給人挑戰）。
5. **一頁一個想法** 一頁只承載一個論點；要用「而且」就拆兩頁。一頁塞多個重點＝觀眾一個都記不住。
6. **技術/研究 talk 用 Assertion-Evidence** 句子標題陳述該頁訊息（約 8–14 字、≤2 行），
   內文用視覺證據（圖表／示意圖／照片），**禁 bullet list**；口頭即時把那一句展開成數句。
   對照研究顯示其理解與記憶顯著優於傳統 topic+bullet 投影片。
7. **內容定稿才碰視覺** 先把 governing thought、敘事骨架、每頁論點全部敲定，再開工具做頁。
   先美化再想內容＝在錯的東西上拋光。（這也是 talk-craft → slidev-deck-stack 的交棒點）
8. **結尾要明確 CTA，且不靠 live demo** 利用 recency，最後一頁放最想留下的訊息 + 一個明確下一步
   （最多 3 個 takeaway）；任何 live demo 必備援（錄影 + 一頁預期輸出 fallback），別把整場賭在它會動。

> 上面是**可驗的核心**。判斷題（敘事弧怎麼選、contrast 強度、STAR 放哪、受眾校準、訊噪比拿捏）
> 是質性守則，不必然「違反即重寫」，放在選型表與 references 裡——簡報 craft 有客觀底線也有主觀手藝，
> 別把手藝硬塞成鐵則。

## 敘事與框架選型表（選型路由）

| talk 類型 / 需求 | 主框架 | 參考檔 |
|------------------|--------|--------|
| 研究 / conference / 技術 talk | Assertion-Evidence + 結構化論證（argument→data→layout→aesthetics） | [slide-craft.md](references/slide-craft.md)、[talk-types.md](references/talk-types.md) |
| 顧問 / 商業匯報 / 述職 | Minto SCQA + 金字塔 + MECE；BLUF | [narrative-arcs.md](references/narrative-arcs.md)、[talk-types.md](references/talk-types.md) |
| pitch / 投資人 | Kawasaki 10/20/30；Sequoia 10-slide；Raskin 戰略敘事 | [talk-types.md](references/talk-types.md) |
| keynote / 科普 / 對外分享 | Duarte Sparkline + STAR；TED throughline | [narrative-arcs.md](references/narrative-arcs.md)、[delivery.md](references/delivery.md) |
| 數據導向匯報 | Knaflic 六堂課 | [data-viz.md](references/data-viz.md) |
| 技術 demo / 實戰 walkthrough / 資安攻防 | Assertion-Evidence + field-tested 實戰招式（refrain / 進度地圖 / demo 當故事 / kill-chain） | [field-patterns.md](references/field-patterns.md)、[talk-types.md](references/talk-types.md) |
| 不確定要哪種敘事弧 | SCQA / 三幕 / Hero / Sparkline / STAR / BLUF / Raskin menu | [narrative-arcs.md](references/narrative-arcs.md) |

判斷順序：先問「受眾要被**說服**還是被**告知**？」→ 說服走敘事弧（Sparkline / Raskin），
告知走結構化（金字塔 / Assertion-Evidence）；再問「是技術/研究 talk 嗎？」→ Assertion-Evidence；
再問「重點是資料嗎？」→ Knaflic 六堂課；再問「是 pitch 嗎？」→ Kawasaki / Sequoia / Raskin。

## references/ 路由表

按需載入，維持本檔精簡。**動手寫內容前先讀對應檔案。**

| 情境 | 讀這個檔 |
|------|---------|
| 定 governing thought、選敘事弧、金字塔/SCQA/MECE、排 ghost deck / dot-dash | [references/narrative-arcs.md](references/narrative-arcs.md) |
| 要可複製的填空骨架（SCQA / Big Idea / **ghost-deck 交棒物**） | [references/templates.md](references/templates.md) |
| 從主題到 ghost-deck 的端到端走查示範 | [references/worked-example.md](references/worked-example.md) |
| 下 action title、每頁 assertion-evidence、訊噪比、認知負荷、rule of three | [references/slide-craft.md](references/slide-craft.md) |
| 圖表選型、Knaflic 六堂課、Tufte、在圖上點 takeaway、圖表誠信 | [references/data-viz.md](references/data-viz.md) |
| throughline、60s hook、STAR、時間預算、演練、speaker notes、demo 安全網、收尾 | [references/delivery.md](references/delivery.md) |
| 依 talk 類型選框架（研究/顧問/pitch/keynote/數據）、pitch 結構細節 | [references/talk-types.md](references/talk-types.md) |
| 技術 / 實戰 demo talk 的實戰招式（refrain、進度地圖、demo 當故事、延伸類比、計分板、ATT&CK / kill-chain 骨架、資安子節） | [references/field-patterns.md](references/field-patterns.md) |
| 寫前自檢 + **寫後驗收 gate（checklist 逐項過）**、踩到反模式（整頁 bullet、念 agenda、slideument…）、上台前檢查 | [references/anti-patterns.md](references/anti-patterns.md) |
| 要查框架原典 / 來源 / 授權 | [references/sources.md](references/sources.md) |

## 與 AI-SOP-Protocol（ASP）及其他 skill 的關係

本 skill 是**內容／溝通層**（簡報怎麼寫），ASP 是**治理層**（怎麼工作），透過專案 CLAUDE.md
疊加、互不取代。

- **與 `slidev-deck-stack` 互補**：talk-craft 決定「寫什麼／怎麼組織論證」，slidev-deck-stack
  決定「怎麼用 Slidev 把它實作」。標準流程是**先 talk-craft 再 slidev**：先敲定 governing thought、
  敘事骨架、每頁 action title（鐵則 7 的「內容定稿」），再交給 slidev-deck-stack 落成 deck。
  - **交棒物 ＝ ghost-deck artifact**（格式見 `references/templates.md` §3）：deck header
    （`governing-thought` / `talk-type` / `audience` / `arc` / `design-direction`）＋ 每頁一個
    `slide` 區塊（`title` / `assertion` / `exhibit` / `reveal` / `note`）。**欄位是兩 skill 的
    共用契約**，slidev 端的消費規格在其 `references/handoff.md`，欄位字字對齊。
  - **職責切點**：talk-craft 給 `design-direction`（設計**方向**）與**雙語內容**策略（哪種語言寫
    標題／throughline、術語中英處理）；slidev 把 design-direction 對映到實際 theme、把 exhibit
    對映到 layout、並處理中文**字型**落地。
- **與 `visual-web-stack` 並列**：三者都是知識層 skill，各管一個領域（網頁技術棧 / Slidev 機制 /
  簡報內容），互不重疊。
- 品質門檻（G1–G6）、commit 流程、ADR 紀律 → 聽 ASP。
- 衝突時：工作流程聽 ASP；簡報內容與論證聽本 skill；Slidev 實作細節聽 slidev-deck-stack。

在做簡報的專案 CLAUDE.md 加入一行即繼承本規範：

```
本專案簡報內容遵循 talk-craft skill，敘事與論證規範以該 skill 鐵則為準。
```
