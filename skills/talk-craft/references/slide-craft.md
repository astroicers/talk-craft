# 投影片層 — Assertion-Evidence、action title、訊噪比、認知負荷

> 適用：骨架定好後，逐頁把論點寫成頁面。核心一句話：**標題下論點、內文放視覺證據、話由人講。**

## 1. Assertion-Evidence（學術實證派，技術 talk 預設）

**來源**：Michael Alley（Penn State）《The Craft of Scientific Presentations》、assertion-evidence.com；
Garner & Alley 等對照研究（理解與記憶顯著優於 topic+bullet，統計顯著）。

三原則：
1. **以訊息（messages）組織，不是主題（topics）** — 用「這頁要讓觀眾相信什麼」決定一頁，自然剔除無關細節。
2. **用視覺證據支撐，不用 bullet list** — 照片 / 圖表 / 示意圖 / 動畫。
3. **解釋證據時口頭即時組句** — 投影片寫一句，你口頭講六到九句（「fashion sentences on the spot」）。

句子標題（sentence headline）規格：
- 陳述該頁的**單一訊息**，是一句完整的話。
- 約 **8–14 字、≤2 行、左對齊、句首大寫、句尾不加句號**。
- 標題下留白（給內文/證據呼吸）。

為什麼有效：用訊息思考逼你剔除冗料；不照唸 bullet 讓你保持眼神接觸；理論根源是 Mayer 多媒體學習原則
與 Sweller 認知負荷理論。

## 2. Action titles（顧問版的同一件事）

**來源**：McKinsey / Minto 慣例。
- 每頁標題＝一句完整、可驗的**論點**；把所有標題單獨讀完，應等於整份論證（＝ ghost deck test 的另一面）。
- ❌「市場分析」 ✅「市場成長但破碎且競爭激烈」。
- Assertion-Evidence 的「句子標題」與顧問的「action title」是同一件事的兩個傳統，可互通。

## 3. 訊噪比與極簡（Presentation Zen）

**來源**：Garr Reynolds《Presentation Zen》；Duarte《slide:ology》《Resonate》對「slideument」的批判。
- **訊噪比（signal-to-noise）**：每個元素要嘛承載訊息、要嘛刪掉。
- **圖優效應（picture superiority）**：圖比字好記；**留白**與**克制**是設計，不是空。
- **不要做 slideument**：同時當投影片又當文件的東西兩邊都做不好——要書面細節就**另做一份 leave-behind / pre-read**，
  別把所有字塞進投影片。

## 4. 認知負荷（Cognitive Load）

**來源**：Mayer 多媒體原則、Sweller 認知負荷理論。
- **冗餘原則**：別逐字唸投影片上的字（口語＋同字文字互相干擾）。
- **空間鄰近**：標籤/註解放在它解釋的視覺**旁邊**，不要分離。
- **逐步揭露**管理負荷：複雜內容分次出現，講到哪揭到哪（實作對應 `slidev-deck-stack` 的 v-clicks / 逐步 SVG）。

## 5. Rule of three

三個支撐點好記、好排；與 Minto 的「2–4 個論點」相容。需要更多時，先分組再呈現（一次只給一組）。

## 交棒
此頁的圖表怎麼選、怎麼點 takeaway → `data-viz.md`；做成 Slidev 的逐步揭示與行高亮 → `slidev-deck-stack`
的 `animation.md` / `code-and-diagrams.md`。
