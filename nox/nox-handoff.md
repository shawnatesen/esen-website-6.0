# NOX ｜ 整頁 Review ＋ 改寫 Handoff（給設計師 Josh）

**頁面**：`esen-proposal-official.webflow.io/nox`
**這份文件取代**：先前拆散的 `nox-club-page-review.md`、`nox-club-photo-selection.md`、mockup 註記——本檔為 /nox 整頁的**唯一權威 handoff**（含逐段文案、視覺設計、照片對應、合規、連結，一份到底）。

**Mockup 索引**（都在 `mockups/`，PNG 可直接預覽）：
| 段落 | HTML | PNG |
|---|---|---|
| 整頁示意 v2 | `nox-club-mockup.html` | `nox-club-mockup-v2.png` |
| ④ THE METHOD 三支柱 | `nox-method-mockup.html` | `nox-method-mockup.png` |
| ⑤ DATA-CENTRIC 散點→曲線 | `nox-data-mockup.html` | `nox-data-mockup.png` |
| ⑥ TRANSFORMATION 年度時間軸 | `nox-transformation-mockup.html` | `nox-transformation-mockup.png` |
| ⑩ RECOVERY TECH 卡片版型 | `recovery-tech-mockup.html` | `recovery-tech-mockup.png` |

---

## 0. 這頁要說的一件事

> **NOX ＝ 為現代高階領導者打造的私人醫療團隊。**
> 用獨家基因檢測 ＋ 全方位 AI 數據 ＋ 一支真正在乎你的專業團隊，幫你抗衰老、把狀態維持在巔峰。
> 加入 ĒSEN，加入 the Club.

**頁面權重：95% 講「私人醫療團隊」，5% 講「社群」。**
社群（ĒSEN Club 的人與聚會）是收尾的一個 grace note，不是主角。先前版本社群照片太重，會稀釋高端醫療感——這版明確收斂。

**TA／ICP**：高成就的領導者。他們厭倦了當自己的「健康專案經理」——自己查、自己約、自己拼湊一堆專家意見，卻沒有一個人真正把他的健康扛起來、真正在乎。NOX 賣的就是「終於有一支團隊接手」。

**敘事弧（整頁順序就照這個走）**：
私人醫療團隊 → 方法（基因＋數據＋團隊） → 數據驅動 → 改變與蛻變 → 專屬與稀有 → 最後才是 網絡與連結 → 申請。

**Brand voice**：依 `~/projects/esen-marketing/claude-skills/brand-voice/`——warm authority、邀請而非推銷、不恐嚇、不誇大；全頁**只保留一句對比句**作 signature。
**《醫療法》合規**：禁「會員限定／頂級／最／第一／根治／無副作用／限時優惠」等；改用「採預約制／名額有限／需事先申請與評估」。設備卡療效字眼一律改衛教式。

---

## 1. 逐段 Review ＋ 改寫稿

### ① HERO — 嚮往（加底圖）
**現況**：純文字 Hero，缺少 premium 視覺重量。
**改**：加滿版底圖 ＋ 暗 scrim 壓字。

- 底圖：**DSC01795**（會所 lounge，深色留白）[看圖](https://drive.google.com/file/d/1mtviWnvaZe-62Ef0YHNwPc5PYaYo9DFP/view) `1mtviWnvaZe-62Ef0YHNwPc5PYaYo9DFP`
- Eyebrow：`NOX · ĒSEN CLUB`
- H1：`影響力，從健康開始。`
- Sub：`為現代高階領導者打造的私人醫療團隊——用最好的狀態，繼續影響與體驗世界。`
- 主 CTA：`申請加入 NOX` → Typeform｜次 CTA：`了解更多`（錨點到下方）

> 🔴 現在主／次 CTA 都連 `#`，要接真實連結（見 §3）。

---

### ② 數字 STRIP — 一眼的份量（保留）
`4` 生活醫學維度 · `365` 天全年陪伴 · `4×` 年度醫師追蹤 · `1` 純邀約制社群
（數字用 Titanium。「純邀約制」合規上沒問題，是事實陳述，非招徠誘因。）

---

### ③ PRIVATE CARE — 私人醫療團隊〔情感核心・這頁主戲〕
**這是整頁最重的一段。** 直接打在 TA 的痛點上。

- Eyebrow：`Private Care · 私人醫療團隊`
- H2：`不必再當自己的健康專案經理。`
- 內文：
  > 你習慣把每件事做到最好，卻發現最難管理的，是自己的健康。
  > 在 NOX，一支跨科別的專業團隊接手——基因檢測師、醫師、營養師、健康管理師，長期陪著你。該做什麼、什麼時候做，由團隊判斷；你只要把健康交給我們，把時間留給真正重要的事。
- 照片：**DSC01307**（一對一深談，最像私人照護）[看圖](https://drive.google.com/file/d/17yfxj3gLPvsDeg9DVF6mnsI0M2Bt9RlE/view) `17yfxj3gLPvsDeg9DVF6mnsI0M2Bt9RlE`
  *（若日後有更好的「醫師＋會員」實照，優先替換。）*

> 設計：左文右圖（或上文下圖），給這段最大的呼吸空間。這是全頁的情感支點。

---

### ④ THE METHOD — 我們怎麼做到〔方法〕
**承接「團隊接手」之後，回答「靠什麼」。** 三根支柱，不要寫成功能清單，寫成「你會得到什麼」。

- Eyebrow：`The Method · 我們的方法`
- H2：`看得夠深，才談得上預防。`
- 三欄（沿用 NOX Experience 的 Know Your Body／Dedicated Team 精神，補上資料軸）：
  1. **獨家基因檢測**：從你的基因起點出發，看見一般健檢看不到的長期風險與體質傾向。
  2. **全方位 AI 數據**：把檢測、生理指標與生活數據整合成一份完整的身體地圖，持續更新。
  3. **有溫度的專業團隊**：數據只是起點，真正的價值是有一支團隊讀懂它、為你判斷下一步。

**🎨 視覺設計（給 Josh）** — 預覽 `mockups/nox-method-mockup.png`
- **版式**：置中 Eyebrow ＋ H2，下方三欄等寬。**不要用卡片框**——欄與欄之間用 1px hairline（`rgba(255,255,255,.12)`）分隔，維持編輯感、不要「功能卡」的廉價感。深色底（沿用 Nox `#0c0a09`）。
- **每欄結構（由上而下）**：序號 `01／02／03`（serif、Titanium、小字 letter-spacing 拉開）→ aura 母題（78px）→ H3 serif 標題 → 內文（max-width ~280px，置中）。
- **aura 母題（品牌唯一插畫元素，三欄各異但同語彙）**：
  - `01 基因` = 一個圓環 ＋ 正中心一個實心點 →「起點／種子」。
  - `02 數據` = 三層同心圓（外到內透明度遞減）→「資料一層層疊加」。
  - `03 團隊` = 兩個圓環左右交疊 →「連結／照護」。
  - 線條 1px、色 Titanium `#9B8062`，透明度 .2–.5；**不要填色、不要 icon、不要陰影**（符合 borders-over-shadows、aura circle 唯一母題）。
- **底部 journey line**（可選但建議）：`基因起點 —•— 持續數據 —•— 團隊判斷` 一條極細 Titanium 連線，把三支柱串成一條路徑，呼應「方法是一條流程，不是三個功能」。
- **互動**：hover 僅 opacity 0.7，無放大、無變色。
- **RWD**：≤820px 三欄改直向堆疊，hairline 隱藏。
- **字級**：H2 clamp(30–46px)；H3 23px；內文 15px／行高 1.95（深色底要夠鬆才耐讀）。

---

### ⑤ DATA-CENTRIC — 數據驅動的判斷〔數據軸〕
**把「AI 數據」講成決策品質，而不是科技炫技。**（依你先前指示：data-first 不downplay，但不過度堆 App＋穿戴。）

- Eyebrow：`Data-Centric · 以數據為依據`
- H2：`每一個建議，都有依據。`
- 內文：
  > 我們不靠感覺、也不靠通則。你的每一份數據都會被持續追蹤、彼此對照——讓團隊在問題還只是趨勢時就看見它，並隨你的身體變化調整策略。健康管理，從一次性的健檢，變成一條持續更新的曲線。
- 兩個對照標籤：`一次性健檢｜一年一次的快照` × `NOX 持續追蹤｜一條不斷更新的曲線`

**🎨 視覺設計（給 Josh）** — 預覽 `mockups/nox-data-mockup.png`
- **版式**：左文右圖（≈0.9 : 1.1）。左欄 Eyebrow＋H2＋內文＋兩個對照標籤；右欄一塊深色 viz 區（1px 邊框、`radius 6px`、微漸層底 `#15110d→#0c0a09`）。
- **viz 核心概念（一張圖講完數據主張）**：左側三個**零散的點**（＝過去一次性健檢）→ 向右收斂成一條**緩緩上升的連續曲線**（＝NOX 持續追蹤），曲線末端用 **aura circle**（實心點＋兩圈外環）標記「此刻」。
- 線條 1.6px Titanium；節點為空心小圈（填底色＋Titanium 描邊）。**絕對不要**放真實儀表板/數字截圖——太工具感、稀釋質感。
- 角落兩個極小灰字標：左上 `過去：零散的點`、右下（Titanium）`NOX：持續的曲線`。
- **RWD**：≤860px 改上下堆疊（文上、viz 下）。

---

### ⑥ TRANSFORMATION — 改變與蛻變〔成果〕
**讓 TA 想像「半年、一年後的自己」。** 對應原 NOX Year 的節奏內容，但敘事化。

- Eyebrow：`Transformation · 一年的改變`
- H2：`不是更努力，而是狀態回來了。`
- 內文：
  > 加入 NOX 的第一年，團隊會陪你走過完整的循環——深度評估、個人化策略、定期追蹤與調整。一年 4 次醫師追蹤、365 天的團隊陪伴，讓改變不是一時的衝刺，而是累積下來、看得見的曲線。

**🎨 視覺設計（給 Josh）** — 預覽 `mockups/nox-transformation-mockup.png`
- **版式**：置中標題區（Eyebrow＋H2＋一句 sub）→ 三個數字（`4×` 年度醫師追蹤・`365` 天團隊陪伴・`1` 完整年度循環，數字 serif Titanium）→ 下方一條**水平年度時間軸**。
- **時間軸**：一條 Titanium 細線橫貫，上方疊一條**微微上升的曲線**（＝累積的改變、狀態回升）；線上 **4 個季度節點**（空心圈），對應 4× 醫師追蹤。
- **4 個節點文案（Q1–Q4）**：
  - Q1 `深度評估`：基因檢測與全方位數據，建立你的身體基準。
  - Q2 `個人化策略`：團隊依數據，為你安排專屬的調整方向。
  - Q3 `定期追蹤`：醫師追蹤與數據回看，確認方向、即時微調。
  - Q4 `回顧與調整`：檢視一年的曲線，定下下一階段的節奏。
- 若沿用既有「NOX Year 6 項」，可把 6 項分配到對應季度做展開細節。
- **RWD**：≤860px 節點改 2×2。

---

### ⑦ EXCLUSIVITY — 專屬與稀有〔門檻〕
**這裡是「為什麼不是人人都能進」——但要合規。** 不講「會員限定／頂級」，講「為了照顧品質，名額本來就有限」。

- Eyebrow：`By Application · 申請與評估制`
- H2：`照顧得夠深，人數就不能多。`
- 內文：
  > NOX 採申請與評估制。一支團隊能真正照顧好的人有限，所以我們寧可把名額留給準備好把健康當一回事的人。這不是門檻，是對每一位會員的承諾。
- 合規註：避免「創始席位／限時」等促銷暗示；「名額有限」可，但語氣是「為品質」而非「製造搶購」。

---

### ⑧ ĒSEN CLUB — 網絡與連結〔社群・只此一段，收斂〕
**社群全頁只出現這一段，放在最終 CTA 前。** 醫療實質之後的「還有歸屬感」收尾。

- 滿版底圖：**DSC08157**（暖調晚宴）[看圖](https://drive.google.com/file/d/14ylajxhjUJa2yuBSC-M9_w-iBXVFcalT/view) `14ylajxhjUJa2yuBSC-M9_w-iBXVFcalT` ＋暗 scrim，文字置中
- Eyebrow：`ĒSEN Club`
- H2：`在私人醫療團隊之外，還有一群同頻的人。`
- 一句見證：`「他們從不急著推銷，而是用最適合我的方式陪著我。」`
- 連結：`了解 ĒSEN Club →`（連 `club.esenmedical.com` 或 `/base`）

> 其餘 11 張活動照（原 `nox-club-photo-selection.md` 清單）**暫不上頁**，留作社群頁／未來用。不做大 gallery。

---

### ⑨ 結尾 CTA — 申請
- Eyebrow：`By Application`
- H2（品牌定位句）：`加入 ĒSEN，加入 the Club.`
- 主 CTA：`申請加入 NOX` → Typeform

---

### ⑩ RECOVERY TECH（原 FACILITIES）
**🎨 視覺設計（給 Josh）** — 預覽 `mockups/recovery-tech-mockup.png`
- 深色「1 feature（上，滿寬）+ 3（下）」editorial grid，4 張卡。深色讓這段成為頁面的 Nox beat。
- 卡片：照片滿版 ＋ 底部暗 scrim 壓字（serif 標題＋一行說明）。hover 僅 opacity，純展示**不外連**。
- 段落框：Eyebrow `Recovery Tech · 會員專屬的恢復科技`｜H2 `恢復，也是照顧的一部分。`｜引言 `Club 限定的恢復設備，由團隊依你的身體狀況安排使用——讓身體在高強度的日常之外，有真正修復的空間。`（「由團隊安排」扣回私人醫療團隊主軸，也讓設備合規。）

**4 張卡文案 ＋ 照片**：
| # | 卡片 | 文案（draft） | 照片 ID |
|---|---|---|---|
| 1 ★feature | 冷凍艙 | 全身低溫環境，幫助身體進入恢復節奏。 | [看圖](https://drive.google.com/file/d/1WmnS4_owZT6qa1fDyyZF5lvyB__qbIBH/view) `1WmnS4_owZT6qa1fDyyZF5lvyB__qbIBH` |
| 2 | 冰浴 & 桑拿 | 冷熱交替，是常見的恢復方式之一。 | [看圖](https://drive.google.com/file/d/1pJhX8kaBp0fOfTv5K2eqhG7EaJPrcKXd/view) `1pJhX8kaBp0fOfTv5K2eqhG7EaJPrcKXd` |
| 3 | 紅光療法 | 以紅光與近紅外光，溫和地陪伴恢復過程。 | [看圖](https://drive.google.com/file/d/17-VWj3q_btBU-62JKyxkUZD-jAoVAPfj/view) `17-VWj3q_btBU-62JKyxkUZD-jAoVAPfj` |
| 4 | 身心共振 | 透過溫和的頻率與律動，幫助身心回到放鬆的節奏。 | [看圖](https://drive.google.com/file/d/1hYodITAGAI9bhxVxGRdxa3H4dc6ldTNT/view) `1hYodITAGAI9bhxVxGRdxa3H4dc6ldTNT` |

> **VO₂max 已移出本段** → 歸 CAPABILITIES 檢測群組：`VO₂max 心肺適能檢測：了解身體的有氧表現，作為恢復與訓練的基準。`
> 冷凍艙 feature 卡 `object-position:center 26%`（讓人像/霧氣入鏡，不要只剩艙門）。
> 完整版（含信義頁用法、THE SPACE 區隔）：`recovery-tech-handoff.md`。

- 🔴 標題 FACILITIES → **RECOVERY TECH**（與信義頁統一）。
- 🔴 舊版 ×7 卡片死連結 `#` → 取消連結（純展示）。
- 🔴 合規：舊文案關鍵字「極速恢復／消炎止痛／抗發炎／排除毒素／免疫調節／淨化血液」屬療效宣稱——已全數改為上表的衛教式描述。

### ⑪ BASE / NOX 方案卡（保留）
- 文案保留。🔴 CTA 連結現全是 `#`：申請加入／方案比較／預約門診／申請候補 → 接真實連結（見 §3）。

---

## 2. 段落順序總表（給 Josh 直接照排）

| # | 段落 | 角色 | 動作 |
|---|---|---|---|
| 1 | HERO | 嚮往 | 加底圖 ＋ 改 Sub ＋ 接 CTA |
| 2 | 數字 STRIP | 份量 | 保留 |
| 3 | PRIVATE CARE | 情感核心 | **新增・主戲** |
| 4 | THE METHOD | 方法 | 由 NOX Experience 改寫 |
| 5 | DATA-CENTRIC | 數據 | 新增 |
| 6 | TRANSFORMATION | 成果 | 由 NOX Year 改寫 |
| 7 | EXCLUSIVITY | 門檻 | 新增（合規） |
| 8 | ĒSEN CLUB band | 社群 | **收斂成一段** |
| 9 | 結尾 CTA | 申請 | 改定位句 |
| 10 | RECOVERY TECH | 設備 | 改標題＋合規 |
| 11 | 方案卡 | 方案 | 保留＋修連結 |

---

## 3. 🔴 必修彙整（連結 ＋ 合規）

**連結**（全頁 CTA 現在都是 `#`）：
- 申請加入 NOX／申請候補 → Typeform `https://form.typeform.com/to/rxgPCqGv`
- 探索信義診所 → `/xin-yi-flagship`
- 方案比較 → `/base`
- 預約門診 → `/consult`
- RECOVERY TECH ×7 卡片 → 取消連結

**合規**：
- FACILITIES → RECOVERY TECH（標題統一）。
- 設備卡療效字眼改衛教式。
- 全頁禁「會員限定／頂級／最」等；用「申請與評估制／名額有限」。

---

## 4. 提醒
- 照片含活動賓客人臉，上線前確認**肖像權**（尤其非 KOL 的一般賓客）。
- 全部文案先當 **draft（人味待校）**，正式上線前過一次 human-voice 標準（特別留意 AI 慣用語、對句只留一句）。
- No More Red／Talks／所有活動 多數子夾對我存取為空；若要更多活動照，設「知道連結皆可檢視」。
