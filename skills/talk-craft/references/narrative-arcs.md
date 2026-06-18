# 敘事與結構 — 金字塔、敘事弧、ghost deck

> 適用：開新簡報、定 governing thought、選敘事骨架。**先把骨架敲定，再做任何一頁。**

## 1. 先定 governing thought（單一訊息）

整場簡報回答**一個**問題，核心是**一句完整的論點句**（answer，不是主題）。
- ✅ 「零信任分段讓橫向移動在 90 天內降到趨近零」
- ❌ 「零信任架構介紹」（這是主題，不是論點）

一句話講不出來，代表還沒想清楚——這時做頁只是把混亂視覺化。（Duarte 稱 big idea；Minto 稱 governing thought。）

## 2. Minto 金字塔原理 + SCQA + MECE

**來源**：Barbara Minto《The Pyramid Principle》（McKinsey 1970s）。顧問業結構標準。

- **金字塔**：頂端＝單一結論（governing thought）；下方 2–4 個支撐論點；每個論點再由資料/事實支撐。
  - 任一層的想法，都是其下一層想法的**摘要**。
  - 同一組想法要**同抽象層級**，並用四種之一排序：演繹 / 時序 / 結構 / 比較。
- **SCQA 開場**（執行摘要頁就是它）：
  - **S**ituation：受眾會點頭同意的現況。
  - **C**omplication：出現的問題/變化（「so what」）。
  - **Q**uestion：因此要回答的問題（常可隱含，不必明寫）。
  - **A**nswer：你的結論＝金字塔頂端。
- **MECE**：支撐論點彼此互斥、合起來窮盡（不重疊、不遺漏）。
- **垂直邏輯**（標題↔內文的 Q&A）＋ **水平邏輯**（同層論點的排序）。
- **戒律**：不要放無結構的「Background」「Introduction」段——任何內容都掛在某個問題之下。

## 3. 敘事弧 menu（依受眾與目的選一個當骨架）

沒有唯一正解；選最貼合「受眾要被說服 vs 被告知」者：

| 弧 | 形狀 | 適用 | 來源 |
|----|------|------|------|
| **SCQA / SCR** | 現況→衝突→問題→答案 | 商業匯報、決策備忘、技術提案 | Minto |
| **三幕結構** | 鋪陳→messy middle（衝突）→解決 | 通用、keynote | 戲劇 / Duarte |
| **Hero's Journey** | **受眾是英雄，你是嚮導** | 願景、產品、號召改變 | Campbell / Duarte |
| **Duarte Sparkline** | 在「what is / what could be」間反覆擺盪，終點 new bliss | 說服、發表會、募資 | Duarte《Resonate》 |
| **STAR** | Situation-Task-Action-Result | 述職、個案、面試 | 行為敘事 |
| **BLUF** | Bottom Line Up Front（結論先講，極短） | 極短匯報、高層 | 軍事/顧問 |
| **Raskin 戰略敘事** | 見下 §5 | pitch、產品定位 | Andy Raskin |

判斷：**被說服**（要對方行動/相信）→ Sparkline / Hero / Raskin（有張力、有情感）；
**被告知**（要對方理解/決策）→ 金字塔 / SCQA / Assertion-Evidence（清楚、可掃描）。

## 4. Ghost deck / Dot-dash（先寫骨架，不做頁）

**來源**：academic-pptx（ghost deck test）、Olito-Labs/slides（dot-dash）、Minto。

流程：
1. **只寫每頁的 action title**（完整論點句），條列成一份骨架。
2. **把標題從頭到尾串起來唸**——必須像一段連貫的論證；讀不通就**重排骨架**。
3. 每頁套 **So What? 測試**：一句話連不回 governing thought 就**砍掉那頁**。
4. **拿骨架去給同事/主管挑戰**，結構穩了才做頁。改結構便宜，改幾十頁貴。
5. 為每頁標一個 exhibit 型別（圖表/示意圖/程式碼/數字），決定它需要什麼視覺證據——這份骨架直接交棒給 `slidev-deck-stack`。

## 5. Duarte Sparkline 與 Andy Raskin 戰略敘事（兩個說服型骨架的細節）

**Sparkline（Duarte《Resonate》）**：在「what is」（現況）與「what could be」（願景）之間**反覆來回**，
靠 **contrast（張力）** 推進，終點是「new bliss」（你的提案被採納後的世界）。兩大反模式：純資料的「報告」、
純煽動的「pitch」——都缺 contrast。

**Raskin 戰略敘事**（pitch/定位特別有效）：
1. 點名世界正在發生的一個**大變化**（不是先講你的產品）。
2. 指出會有**贏家與輸家**（製造利害）。
3. 描繪 **promised land**（採用後的美好，但具體、可衡量）。
4. 把功能當成**克服阻礙的「魔法禮物」**逐一介紹。
5. 給出**證據**證明你能讓這故事成真。

## 與 slide / data / delivery 的交棒

骨架（本檔）定好後：每頁怎麼下標題與放證據 → `slide-craft.md`；圖表怎麼做 → `data-viz.md`；
怎麼講、怎麼演練 → `delivery.md`；依 talk 類型套哪個框架 → `talk-types.md`。
