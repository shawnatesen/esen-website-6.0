# ĒSEN Services 三頁 — 結構交付（給設計師 Josh）

> **語言狀態**：本檔文案為 **draft，聚焦結構**。用字之後會經 brand-voice humanizer 再過一輪；先確認**架構、區塊、版型、CMS 綁定**是否可建。
> 三頁：`/service/screen`（檢測）｜`/service/treatment`（調養）｜`/service/live-track`（追蹤，原 /service/wellness，記得 301）

---

## 0. Josh 的問題（記錄）

> 「目前用 CMS，所以理論上三個頁面的架構為一致的，但我目前看規劃三個頁面會長得完全不一樣。如果是這樣就把他們都改成 static 的頁面；但如果走這條，麻煩給我每頁詳細的內容跟所有文案。還是你有其他想法？」

**回答：你的觀察對——三頁結構本來就不同（各頁任務不同）。但我建議走 hybrid，不要「單一 CMS 模板」也不要「三頁全手工 static」。**

三頁本質：
| 頁 | 結構本質 | 任務 |
|---|---|---|
| Screen 檢測 | 目錄＋漏斗（招牌 A ＋ 熱搜 B → 導流） | sell 招牌＋吃 SEO |
| Treatment 調養 | 療程卡片 grid | 展示療程廣度 |
| Live Track 追蹤 | 團隊／關係／數據引擎的敘事 | 傳遞長期陪伴 |

---

## 1. 建議架構：Hybrid（服務項目走 CMS，頁殼走 static 元件）

**核心：把「服務項目（會愈長愈多的資料）」跟「頁面骨架（只有 3 個、各不同）」分開。**

- **服務項目 → 一個 CMS Collection**（見 §2）。以後新增檢測／療程，你不用動頁面，Shawn 在 CMS 加一筆即可。
- **三頁 → static 頁殼，用一套共用 section 元件拼**（見 §3）。每頁挑自己要的區塊；需要清單的地方綁 CMS。

好處：品牌/視覺一致（同一套元件）＋ 每頁結構自由 ＋ 未來擴充只加 CMS item。
> 若團隊只想純 CMS vs 純 static 二選一：選 **static 頁殼 ＋ CMS 管項目**，別把三頁塞進單一 CMS 模板。

---

## 2. CMS Collection：`Service Items`

一個 Collection 裝所有檢測與療程項目。頁面用 filter 取用。

| 欄位 | 型別 | 說明／選項 |
|---|---|---|
| `name_zh` | Text | 中文名（e.g. ĒSEN 360° 基因檢測） |
| `name_en` | Text | 英文/招牌名（e.g. Genetics 360） |
| `service_type` | Option | `檢測 Screen`／`療程 Treatment` |
| `tier` | Option | `招牌 Signature`／`熱搜 Popular`／`—`（療程可留空） |
| `category` | Option | 分類 tag（療程：NUTRIENT IV／REGENERATIVE／PHOTOBIOMODULATION／DETOX／BLOOD／HORMONE／RECOVERY；檢測：基因／血液功能／影像／單項） |
| `description` | Text | 一句描述（draft，⚠️ 部分待合規，見 §6） |
| `symptom_group` | Text | 適用症狀群 |
| `availability` | Multi-option | `大安`／`信義·Club`／`兩院區` |
| `featured` | Switch | 是否頁首精選（4 張） |
| `order` | Number | 排序 |

**要輸入的項目（初始資料）＝ 下方各頁「CMS 清單」列的內容**（§4、§5）。Live Track 頁幾乎不吃這個 Collection。

---

## 3. 共用 Section 元件（建一次，三頁重用）

1. **Service Hero** — Eyebrow(EN)＋H1(中文)＋一句 sub＋（可選底圖）。每頁換文字。
2. **Section Intro** — eyebrow＋H2＋lead 一段。
3. **Service Card（CMS-bound）** — name_zh／name_en／category tag／description／symptom_group／availability chip。
4. **Featured Card** — Service Card 的放大變體（頁首精選 4 張）。
5. **Availability Chip** — `大安` / `信義·Club` 小標。
6. **Membership Invite Band（輕量）** — 「更深的陪伴，屬於 ĒSEN Club」→ BASE / NOX。三頁共用。
7. **Closing CTA（共用・已改合規）** — 見 §7。

版型語彙統一：Aura 白底為主、borders over shadows、radius 2px、hover 只用 opacity、欄間 1px hairline、少用 icon（Lucide 1.25 stroke）。

---

## 4. 頁面結構 — SCREEN（檢測）`/service/screen`

static 殼 ＋ 2 個 CMS 清單。

| # | 區塊 | 元件 | 內容（draft） |
|---|---|---|---|
| 1 | Hero | Service Hero | Eyebrow `Screen · 檢測`／H1 `看見，別人看不到的身體。`／sub `從基因到全年數據，把看不見的風險變成看得見的地圖。` |
| 2 | Intro | Section Intro | H2 `看得夠深，才談得上預防。`＋一段：先天基因＋後天全年數據＝一份會更新的健康基準。 |
| 3 | **招牌主推 A** | Section Intro ＋ Featured Card grid | CMS list：`service_type=檢測 & tier=招牌`。見下表 A。 |
| 4 | **熱搜常見 B** | Section Intro ＋ Service Card grid（較密） | CMS list：`service_type=檢測 & tier=熱搜`。見下表 B。 |
| 5 | 導流句 | 文字帶 | `單項檢測，也是健康藍圖的一塊。ĒSEN 用一次完整評估，把碎片拼成全貌。` |
| 6 | Availability | Availability Chip | 大安（開放）＝常規健檢／基礎血液／影像／熱搜單項；信義·Club＝360 基因／Assess Plus／VO₂max／自律神經·腦波／Assess Pro。 |
| 7 | Membership | Invite Band | 共用 |
| 8 | CTA | Closing CTA | §7 |

**CMS 資料 — A 招牌（tier=招牌）**
| name_zh | name_en | category | description(draft) | availability |
|---|---|---|---|---|
| ĒSEN 360° 基因檢測 / Pro | Genetics 360 / Pro | 基因 | 從 DNA 讀懂先天體質（癌症・心血管・代謝・神經退化等關鍵標記）。Pro＝更完整組合。 | 信義·Club |
| ĒSEN Assess / Assess Plus | Assess / Plus | 血液功能 | 全年度精準檢測：120+ 項血液生化與功能醫學，建立並逐年更新健康基準線。 | 兩院區 |
| VO₂max 體適能評估 | VO₂max | 影像/功能 | 心肺適能檢測，了解身體有氧表現與恢復基準。 | 信義·Club |
| 自律神經與腦波 | Neuro | 功能 | 自律神經與腦波評估，理解壓力與精神狀態。 | 信義·Club |
| 深度影像（超音波） | Imaging | 影像 | 進階超音波影像評估。 | 信義·Club |

**CMS 資料 — B 熱搜（tier=熱搜，接 SEO）**
| name_zh | category | availability |
|---|---|---|
| 過敏原檢測 | 單項 | 大安 |
| 男性／女性賀爾蒙檢測 | 單項 | 大安 |
| 代謝營養素檢測（維生素・微量元素） | 單項 | 大安 |
| 腸道菌相檢測 | 單項 | 大安 |
| 重金屬檢測 | 單項 | 大安 |
| 癌症風險基因檢測 | 單項 | 大安 |
| 情緒壓力／自律神經檢測 | 單項 | 大安 |
> 熱搜層描述 draft 從簡（一句衛教式即可）。可選：做關鍵字研究補上台灣人實際搜尋詞，讓這層吃 SEO。

---

## 5. 頁面結構 — TREATMENT（調養）`/service/treatment`

static 殼 ＋ 1 個 CMS 清單（療程 grid）。

| # | 區塊 | 元件 | 內容（draft） |
|---|---|---|---|
| 1 | Hero | Service Hero | Eyebrow `Treatment · 調養`／H1 `依你的數據，醫師為你決定。`／sub `一站式全方位抗衰老療程——不是菜單，是依數據與基因做的醫療決策。` |
| 2 | 精選 4 | Featured Card grid | CMS list：`service_type=療程 & featured=true`。建議：BOOST、PRP、HRT、Recovery。 |
| 3 | 全療程 grid | Service Card grid（可依 category 篩選） | CMS list：`service_type=療程`。見下表。 |
| 4 | Availability | Availability Chip | 每卡帶院區 chip。 |
| 5 | Membership | Invite Band | 共用 |
| 6 | CTA | Closing CTA | §7 |

**CMS 資料 — 療程（service_type=療程）**
| name_zh | category | description(draft) | symptom_group | availability | featured |
|---|---|---|---|---|---|
| ĒSEN BOOST 營養點滴 | NUTRIENT IV | 營養直達，劑量配方由醫師依數據決定 | 疲勞・免疫低下・能量補給 | 兩院區 | ✅ |
| ĒSEN PACK 個人化營養品 | SUPPLEMENT | 依檢測結果，由醫師藥師配專屬組合 | 客製（依檢測） | 兩院區 | — |
| PRP 增生療法 | REGENERATIVE | 自體高濃度血小板，支持修復與組織再生 | 組織修復・關節・運動傷害・再生力 | 兩院區 | ✅ |
| ILIB 靜脈雷射 | PHOTOBIOMODULATION | ⚠️ 見 §6（Josh 註記：拿掉／換掉） | — | — | — |
| 螯合排毒療法 | DETOX | ⚠️ 見 §6（療效字待合規改寫） | 重金屬・排毒 | 大安 | — |
| 血液淨化療法 | BLOOD | ⚠️ 見 §6（療效字待合規改寫） | 排毒淨化 | 大安 | — |
| HRT 賀爾蒙補充療法 | HORMONE | 精準恢復荷爾蒙平衡（女 Oestrogel／男 Androgel·Nebido） | 疲勞・情緒・性功能・更年期 | 兩院區 | ✅ |
| ĒSEN Recovery 系列 | RECOVERY | 冷凍艙／紅光／高壓氧整合 | 發炎・運動表現・恢復・抗老 | 信義·Club | ✅ |

---

## 6. 頁面結構 — LIVE TRACK（追蹤）`/service/live-track`

幾乎全 static（敘事頁），無／極少 CMS。

| # | 區塊 | 元件 | 內容（draft） |
|---|---|---|---|
| 1 | Hero | Service Hero | Eyebrow `Live Track · 追蹤`／H1 `把長期照顧，變成每一天。`／sub `一支溫暖的專屬團隊，把持續變更好變成可持續。` |
| 2 | 照護團隊 | 靜態區塊 | 跨科別醫師 ＋ 健康管理團隊（健康秘書・健康顧問・資深護理師・抗衰老主治醫師）。 |
| 3 | Wellness · 生活醫學諮詢 | 靜態區塊 | 營養師與心理師，把情緒・睡眠・運動・營養變成可執行日常（ĒSEN 4 Pillar）。 |
| 4 | ĒSEN CARE 全年管理 | 靜態區塊 | 一年的計畫，不是一次看診；季度回診、團隊依數據持續調整。 |
| 5 | ĒSEN Intelligence · 健康數據引擎 | 靜態區塊〔AI-native 主軸〕 | 基因＋全年檢測整合成一份會學習的健康檔案，AI 找趨勢、醫師行動。（App／穿戴此頁不展開） |
| 6 | Availability | Availability Chip | 開放 vs Club 專屬。 |
| 7 | Membership | Invite Band（此頁可稍重） | 更深的陪伴屬於 ĒSEN Club：BASE＝起點；NOX＝最貼身的私人醫療團隊（信義專屬）。完整比較留 /nox、/base。 |
| 8 | CTA | Closing CTA | §7 |

---

## 7. 共用收尾 CTA（已改合規，取代舊恐嚇文案）

> 舊版「不能再等了…可能會太遲」＝恐嚇＋假急迫，違反 brand voice，移除。

- 標題：`從一次對話開始。`
- 內文：`最好的時機，是身體還沒發出警訊的現在。預約一次初診，讓醫療團隊認識你，再為你規劃下一步。`
- 主 CTA：`預約初次諮詢` → `/consult`｜次要：`了解 ĒSEN Club` → `/nox`

---

## 8. ⚠️ 合規＋內容決策（上線前必處理，與 humanizer 語言潤飾分開）

1. **ILIB 靜脈雷射**：Josh 已註記「拿掉／靜脈雷射的都換掉」。→ **請 Shawn 拍板**：整項移除，還是保留改衛教式描述？（目前結構先留位標 ⚠️）
2. **螯合排毒／血液淨化**：描述有療效宣稱（排除毒素／過濾毒素）。依《醫療法》改衛教式（描述作法，不承諾結果），或降級處理。
3. **命名統一**：追蹤頁英文＝**Live Track**（不是 Thrive；舊文件第六段的 Thrive 已作廢）。
4. **代表性服務重複卡**：舊版三頁各有一張重複卡，改用各頁 featured 清單後即解。
5. 命名：三頁統一「伊生大安診所／伊生信義診所」；血液檢測項目統一 **120+**。

> 以上是**合規/內容決策**（法規層級），不等 humanizer；語言用字才等 humanizer。
