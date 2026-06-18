# Worked example — 從主題到 ghost-deck 的端到端走查

> 適用：第一次用本 skill、或要校準每一步產出該長什麼樣。**示範的是方法論的文字產出
> （ghost-deck 骨架），不是成品投影片**——成品由 slidev-deck-stack 落地。

假設主題：一場 30 分鐘技術 conference talk，「容器逃逸如何一路接到雲端接管」。

## Step 1 — governing thought（鐵則 1）
> **一個對外 web 漏洞，就能從容器一路逃到雲端 root——破口不在密碼強度，在設定。**

過關判準：能一句話講完、是「答案」不是「主題」。

## Step 2 — 選敘事弧（narrative-arcs §3）
逐步推進的實戰走查 → 選**旅程 / 走查弧（kill-chain）**（見 field-patterns）。
理由：受眾要跟著「一步一步打進去」的張力，不是被條列告知。

## Step 3 — SCQA 開場（templates §1）

```text
S：企業把服務搬上雲、容器化，周邊防護買好買滿
C：但一個對外 web 漏洞 + 一個容器設定錯誤，就能逃出容器
Q：逃出來之後，離雲端 root 還有多遠？
A：比你想的近——20 分鐘、零密碼破解，直接接管。
```

## Step 4 — ghost-deck 骨架（templates §3）

deck header：

```yaml
governing-thought: 一個 web 破口就能從容器逃到雲端 root，關鍵在設定不在密碼
talk-type:         security
audience:          雲端/DevOps 工程師 · 已知容器與雲、低估設定風險 · 最怕「我也中」
arc:               旅程
design-direction:  暗色終端
```

頁（節選，實際約 12 頁）：

```slide
title:     周邊買好買滿，破口還是在一個 debug 頁
exhibit:   diagram
note:      先立「防護很完整」的期待，等下打臉
```

```slide
title:     web RCE 把我們送進一個容器，不是主機
exhibit:   code
reveal:    1) whoami 2) /.dockerenv 存在
```

```slide
title:     20 分鐘、零密碼破解，雲端 root 到手
exhibit:   number
note:      戰果計分板：20 min / 0 密碼 / root
```

串讀檢查：把以上 `title` 由上往下讀，應像「期待 → 逃逸 → 升權 → 接管 → 結論」的連貫論證；
每頁過一次 So-What（narrative-arcs §4）。

## Step 5 — 一頁做成 assertion-evidence（slide-craft）

挑「web RCE 把我們送進一個容器」這頁：
- 句子標題（中文 ~15–25 字）：`web RCE 把我們送進一個容器，不是主機`
- 證據（非 bullet）：一張終端示意，`ls /.dockerenv` 命中 → `exhibit: code`
- 口頭展開 6–9 句：為何先確認「我在容器裡」決定後續路徑。

## Step 6 — 交棒
把這份 ghost-deck（header + 各 `slide` 區塊）交給 slidev-deck-stack；它依 `handoff.md` 把
`exhibit: code` 落成行高亮頁、`exhibit: number` 落成 `fact` 大數字頁、`design-direction: 暗色終端`
對映到暗色 theme。talk-craft 到此為止——**不碰 theme / font / layout 實作**。
