# 實戰招式 field-tested patterns（技術 / 實戰 demo talk）

適用：技術 / 研討會 / 實戰 demo / 攻防展示 talk。這些是從**實際交付過的 conference talk
與公認優秀講題**萃取的 field-tested 模式——**非書本原典**，但每招都盡量對接 skill 既有的
已查證概念（throughline / STAR / contrast / Assertion-Evidence / MECE / Knaflic）。
**擇用即可、不必全上；與鐵則衝突時聽鐵則（尤其鐵則 8 demo 安全網）。**

## 1. 通用招式

1. **Refrain throughline（三點鼓點）** 把 governing thought 拆成 **≤3 句可複述的信條**，
   **開場立 → 每章轉場 / 中段回扣 → 結尾再敲一次**。同一組字、同一順序，重複才記得住。
   → 對接：throughline（delivery.md §1）+ rule of three（slide-craft.md）+ recency（鐵則 8）。

2. **累積式進度地圖 / 定位器** 長走查時用一個**會「長大」或持續存在**的視覺（逐步加長的
   kill-chain 鏈、側欄步驟清單）讓觀眾隨時知道「走到哪、剩多少」。
   - 注意：**不違反「別念 agenda」反模式**——agenda 是開場空念十頁標題；進度地圖是**過程中**的持續定位。
   → 對接：anti-patterns.md（agenda 反模式的正向解）。

3. **Demo / 實戰走查當故事（setup → tension → reveal → payoff）** 把 live demo / 攻防走查寫成
   有張力的故事：**立期待**（全強密碼 / 已上 WAF）→ **製造懸念** → **反轉**（密碼噴灑全敗、
   AI 改走他路 / 同一支攻擊被擋）→ **收割**（戰果計分板）。
   - 必配鐵則 8：錄影備援 + 一頁預期輸出 fallback，別把整場賭在它會動（攻防 demo 尤建議預錄）。
   → 對接：STAR 戲劇化演示（delivery.md §2、§5）+ Duarte contrast（narrative-arcs.md §5）。

4. **延伸類比當解說主軸** 用觀眾**熟悉的領域**承載陌生的技術概念，並讓比喻**一路貫穿**
   （軍事 doctrine → 紅隊；偵探「真相只有一個」→ 偵測；防火牆＝大樓警衛）。
   - 要點：比喻要能**對映回實作**，別只在標題用一次就丟。類比是「把技術講給非專家聽」最有效的技巧之一。
   → 對接：throughline（delivery.md §1）。

5. **抽象 ↔ 具體對照表** 框架 / 理論落地時，用兩欄表把「**概念 ↔ 你的實作**」逐列對齊
   （例：C5ISR 各字母 → 對應的實作工具），證明不是空談。
   → 對接：Assertion-Evidence 的證據形式（slide-craft.md）。

6. **賭注接地（lab → 真實事件）** demo 跑在 lab，但用**具名的真實事件 / 數據**把「這會發生在
   你身上」釘住——抬高 stakes、建立 ethos（例：把自動化攻防接到真實外洩事件；把漏洞接到真實受害者）。
   → 對接：Duarte「what could be」+ STAR 動人故事。

7. **戰果計分板** 收尾用**少數大數字**總結成果（時間 / 完成率 / 人工介入 / 可解釋度），
   一眼可記、可複述。
   → 對接：Knaflic「takeaway 當標題」（data-viz.md）+ STAR 驚人統計。

8. **競品 / 方案定位表** 產品 / 工具型 talk 用一張表沿**關鍵軸**對齊「自己 vs 既有方案」
   （state / auto / framework），點出差異化、避免淪為叫賣。
   → 對接：pitch competition 頁（talk-types.md）；Raskin「贏家與輸家」。

9. **鏡像結構（攻 ↔ 防 / 問題 ↔ 解法）** 先完整走一遍 A（攻擊鏈），再用**同一條結構**走 B
   （逐步偵測 / 防禦），讓兩邊 payoff 對齊、好記。
   → 對接：MECE / 平行結構（narrative-arcs.md §2）。

## 2. 資安 / 紅隊 / 雲端 talk 子節

- **ATT&CK 當結構骨架** 用 MITRE ATT&CK tactic 順序（Initial Access → Execution → … →
  Collection / Impact）當走查骨架、每步標 technique ID——近似 MECE（tactic 間實務上可能重疊），又是觀眾的共通語言。
- **Kill-chain 敘事弧** 偵察 → 突破 → 立足 → 橫向 → 收割，是「旅程型」敘事弧的一種
  （見 narrative-arcs.md §3 弧 menu）。
- **Live exploit 安全網 + OPSEC** live 攻防**強制**錄影 / 預期輸出 fallback（鐵則 8）；展示內容
  **去識別**（打碼 token、用 lab 靶機 / 假帳號），別在台上洩真實 secret。
- **免責聲明頁** 攻防 talk 開場放一頁 disclaimer（僅供教育、授權測試範圍內）。
- **「好人」敘事框架** 把攻擊研究框成**保護受害者**（找洞 → 通報 → 防止損失），給觀眾一個
  有滿足感的弧，而非純炫技。
- **主題語彙一致** 口語 / 視覺主題一致（OPS LOG、時間戳、CLASSIFIED 風）能強化 throughline——
  **視覺落地交給 `slidev-deck-stack`**，本 skill 只定「語彙要前後一致」。

## 3. 可學的公開範例（拿來拆解結構與交付）

研究公認的好講題、直接吸收其結構與節奏；下列各示範一招：

- **Jeep 遠端入侵（Miller & Valasek, DEF CON 23）**──把抽象漏洞變成「記者在高速公路上失控」的人味故事（賭注接地）。
- **Barnaby Jack「Jackpotting ATMs」（Black Hat 2010）**──現場讓 ATM 噴鈔，demo 即高潮（demo 當故事）。
- **Samy Kamkar「How I Met Your Girlfriend」（DEF CON 18）**──流行文化標題＝記憶點（hook 套路）。
- **「The Cavalry Isn't Coming」（DEF CON 21）**──以召喚行動收尾、催生一場運動（CTA / 好人敘事）。
- **Orange Tsai SSRF bypass（Black Hat 2017）**──把單一技法講深講透、成為被廣泛引用的參考（一頁一想法 + 證據）。

> 進一步「best of」清單見 `references/sources.md`（Dark Reading / CSO / Daily Swig 的
> DEF CON & Black Hat 經典講題彙整）。

## 與其他 references 的交棒

骨架選弧 → `narrative-arcs.md`；每頁下標題與證據 → `slide-craft.md`；圖表 → `data-viz.md`；
hook / 演練 / demo 安全網 / 收尾 → `delivery.md`；依類型選框架 → `talk-types.md`。
