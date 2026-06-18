# 資料與視覺 — Knaflic 六堂課、Tufte、圖表誠信

> 適用：簡報裡有圖表/數字時。核心一句話：**圖不是擺資料，是用來證一個論點——把那個 takeaway 直接標在圖上。**

## 1. Knaflic《Storytelling with Data》六堂課

**來源**：Cole Nussbaumer Knaflic（前 Google People Analytics）《Storytelling with Data》。

1. **理解脈絡** — 先定受眾與**單一訊息**（她的「Big Idea worksheet」：一句話講清楚要說什麼）。
2. **選對視覺** — 折線 / 長條 / 表格 / slopegraph / heatmap；**不要圓餅、甜甜圈圖**（大腦難比角度）。
3. **clutter 是敵人** — 刪掉非資料 ink（多餘格線、邊框、標籤）；用 **Gestalt** 知覺原則（鄰近 / 相似 / 對齊）組織；善用留白。
4. **聚焦注意力** — 用 **preattentive attributes（大小 / 顏色 / 位置）** 把眼睛導到重點；顏色要**少而有目的**，
   **直接在圖上點出 takeaway**（例：把超標的那根 bar 標紅 + 加註解）。
5. **像設計師思考** — Affordance（一看就懂怎麼讀）/ Accessibility / Aesthetics / Acceptance。
6. **說故事** — 資料也有起承轉合（beginning-middle-end）；重複強化關鍵；**用 takeaway 當圖表標題**（不是「營收圖」而是「Q4 營收回升 18%」）。

## 2. Tufte

**來源**：Edward Tufte《The Visual Display of Quantitative Information》；〈The Cognitive Style of PowerPoint〉。
- **data-ink ratio** 最大化：墨水盡量花在資料本身。
- **移除 chartjunk**：裝飾性 3D、漸層、無意義網格都砍。
- **small multiples**：多個同尺度小圖並排，比一張塞滿的大圖好比較。
- **sparklines**：行內微型趨勢圖（Duarte 的 sparkline 一詞即借自 Tufte）。
- 警惕：投影片的低解析度會稀釋內容——複雜資料考慮另給書面附件。

## 3. 圖表誠信與選型

- **一張結果頁一個 exhibit**：不要一頁塞三張圖。
- **非零基線＝誤導**：長條圖 y 軸不從 0 開始會放大差異（Knaflic 的經典反例）。
- **把結論寫在圖上**：別讓觀眾自己找重點；標題即 takeaway、關鍵點加 annotation。
- 選型速查：比較類別→長條；趨勢→折線；兩點變化/排名→slopegraph；組成→堆疊長條（**不要圓餅**）；
  相關→散布；密度→heatmap。

## 交棒
把這些圖做進 Slidev（Mermaid / inline SVG / 在圖上逐步點亮）→ `slidev-deck-stack` 的 `code-and-diagrams.md`。
