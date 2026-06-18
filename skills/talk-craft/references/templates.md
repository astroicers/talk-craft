# 範本 templates（SCQA / Big Idea / ghost-deck 交棒物）

> 適用：把方法論落成可複製的填空骨架。**複製 → 填內容**，不必每次自創格式。

## 1. SCQA 執行摘要（四行填空）

開場與執行摘要用 Minto SCQA（見 narrative-arcs.md §2）：

```text
S（Situation 現況）：<雙方都同意的事實背景，不引爭議>
C（Complication 衝突）：<打破現況的變化／問題>
Q（Question 問題）  ：<C 自然引出的那個問題，常隱含>
A（Answer 答案）    ：<你的 governing thought，一句話>
```

## 2. Big Idea worksheet（Knaflic，三欄）

動手排頁前先填（見 data-viz.md §1）：

```text
受眾（who）          ：<是誰／已知什麼／最在意或最怕什麼>
單一訊息（big idea） ：<一句話講清楚要他相信／做什麼>
So-what（行動）      ：<要他離場後做的那件事>
```

## 3. ghost-deck 交棒物（talk-craft → slidev-deck-stack 的契約）

ghost-deck 是 talk-craft 的**最終產出**、slidev-deck-stack 的**輸入**。每頁只寫 action title
＋證據型別，**不碰視覺**（視覺由 slidev 落地）。欄位名是兩 skill 的**共用契約**，slidev 端的
消費規格見其 `references/handoff.md`——**欄位必須字字對齊**。

**deck 級 header（一份一次，放檔案最上方）**：

```yaml
governing-thought: <一句話 big idea>
talk-type:         <research | keynote | pitch | dev-demo | security | workshop | data | consulting>
audience:          <persona 一句：who · 已知 · 最在意/最怕>
arc:               <SCQA | 三幕 | Hero | Sparkline | STAR | BLUF | Raskin | 旅程>
design-direction:  <暗色終端 | 學術襯線 | keynote 大字 | 教學 | 企業 | 通用>
```

> `design-direction` 只給**設計方向**（內容決策），不指定 theme；slidev 端再對映到實際 Slidev
> theme（見 handoff.md）。雙語**內容**策略（哪種語言寫標題／throughline）屬 talk-craft；中文
> **字型**落地屬 slidev。

**per-slide 區塊（每頁一個 fenced `slide` 區塊，順序即頁序）**：

```slide
title:     <action title：完整論點句（鐵則 3）>
assertion: <該頁口頭要展開的單一訊息（鐵則 6）>
exhibit:   <code | diagram | chart | photo | number | quote | section | none>
reveal:    <逐步揭示節點，選填，如「1) 問題 2) 數據 3) 結論」>
note:      <講者提示，選填>
```

**exhibit 值的意義（slidev → layout 對映見 handoff.md）**：
- `code` 程式碼 · `diagram` 流程/架構/時序圖 · `chart` 數據圖表 · `photo` 照片/截圖
- `number` 大數字（戰果計分板） · `quote` 引言 · `section` 章節分隔 · `none` 純標題宣告

**最小範例**：

```slide
title:     強密碼擋不住 AS-REP Roasting
assertion: 五個帳號全強密碼，但其中一個關閉 pre-auth，零憑證就能離線爆破
exhibit:   diagram
reveal:    1) 正常 pre-auth 2) 關閉後 KDC 直接吐 hash 3) 離線爆破
note:      停在「零憑證」這四個字
```

## 交棒
完整走查示範見 `worked-example.md`；slidev 端怎麼把每頁 exhibit 落成 layout、把
design-direction 對映到 theme，見 slidev-deck-stack 的 `references/handoff.md`（欄位字字對齊）。
