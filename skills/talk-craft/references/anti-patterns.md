# 反模式對照表與上台前檢查清單

> 適用：寫完自檢、或感覺哪裡不對。先查表，再回對應 reference 看完整解法。

## 反模式對照表

| 症狀 | 為何錯 | 改成 | 對應 |
|------|--------|------|------|
| 整頁 bullet 照唸 | 口語＋同字文字冗餘，觀眾讀比你講快就放空 | 句子標題 + 視覺證據，口頭即時展開 | slide-craft.md（Assertion-Evidence） |
| 標題只寫主題（「市場分析」） | 讀標題串不出論證，觀眾要自己拼 | action title：完整論點句 | slide-craft.md §2 |
| 先做幾十頁才發現結構不對 | 改頁很貴，整份重排成本高 | 先過 ghost deck，骨架穩了才做頁 | narrative-arcs.md §4 |
| 鋪陳到最後才講結論 | 受眾離席/分心/時間被砍，重點沒講到 | answer-first，第一頁就講答案 | narrative-arcs.md §2 |
| 一頁塞多個重點（用「而且」串） | 觀眾一個都記不住 | 一頁一想法，拆頁 | SKILL.md 鐵則 5 |
| 用「先看 agenda」開場 / 放無結構「Background」段 | 浪費黃金 60 秒、與論證脫節 | 60 秒 hook；內容掛在問題下 | delivery.md §2、narrative-arcs.md §2 |
| 投影片塞滿字當文件用（slideument） | 既不好講也不好讀，兩頭落空 | 投影片放證據；另做 leave-behind/pre-read | slide-craft.md §3 |
| 圓餅/甜甜圈圖、非零基線長條 | 難讀或誤導 | 折線/長條/slopegraph；y 軸從 0 | data-viz.md §3 |
| 圖只擺資料、不點重點 | 觀眾不知道該看哪、結論是什麼 | takeaway 當圖標題、關鍵點加 annotation | data-viz.md §1 |
| 把整場賭在 live demo 會動 | 一掛全毀 | 錄備援影片 + 預期輸出 fallback | delivery.md §5 |
| 最後一張是「謝謝/Q&A」 | 最被記得的位置浪費掉 | 收尾放 takeaway + CTA | delivery.md §6 |
| 字太小、一頁十個概念 | 後排讀不到、認知過載 | ≥30pt、一頁一想法 | talk-types.md §1 |

## 上台前檢查清單

內容（交給 slidev-deck-stack 之前）：
- [ ] 能用**一句話**講出 governing thought
- [ ] 第一頁/執行摘要就是答案（answer-first）
- [ ] 把所有**標題單獨讀完**＝完整論證（ghost deck pass）
- [ ] 每頁只有一個論點，標題是論點句不是主題
- [ ] 技術 talk：每頁是 assertion-evidence（句子標題 + 視覺證據，無 bullet）
- [ ] 每張圖的 takeaway 標在圖上；沒有圓餅圖/非零基線
- [ ] 結尾有明確 CTA 與 ≤3 個 takeaway

交付（上台前）：
- [ ] 對著時鐘大聲跑過整場一遍，沒超時
- [ ] speaker notes 是台詞與提示，不是投影片複製
- [ ] live demo 有錄影備援 + 一頁預期輸出 fallback
- [ ] 確認這份是「現場講」還是「寄出去讀」，密度對得上
