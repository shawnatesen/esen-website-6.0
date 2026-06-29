# ĒSEN Testimonial Carousel — CMS 規格 ＋ 內容（Superpower 風格）

給設計師：用這份在 Webflow 建一個 **CMS Collection「Testimonials」**，每位 KOL 一筆，carousel 綁這個 collection。所有素材都連回原貼文/profile，因此不需另外取得使用同意。

---

## A. CMS 欄位結構（Collection: Testimonials）
| 欄位 | 型別 | 說明／範例 |
|---|---|---|
| `Name` | Plain text | 蔡佩軒 Ariel Tsai |
| `Handle` | Plain text | @arieltsai |
| `Profile URL` | Link | 連到 IG 個人檔案 |
| `Role` 身分 | Plain text | 歌手・創作者 |
| `Treatment` 療程標籤 | Option | 基因檢測／過敏原檢測／營養點滴／PRP／健檢／減重 |
| `Quote` 精選引言 | Plain text | 1–2 句，carousel 卡片主文 |
| `Post URL` | Link | 連到原 IG 貼文/Reel（卡片可點） |
| `Media type` | Option | Reel／Post／Image |
| `Thumbnail` | Image | 卡片縮圖（從貼文截圖或人物照） |
| `Doctor` 主治醫師 | Plain text | 選填，e.g. Dr. Wilson 鄒為之 |
| `Featured` | Switch | 是否優先顯示 |
| `Order` | Number | 排序 |

> Thumbnail 來源：可從貼文截圖，或用「同意使用照片」Drive 資料夾 `1OLY-apoh60e0U7OFDTVeLcRCcINGNmPe`。

---

## B. 內容（7 筆，已可上）

### 1. 冰蹦拉 — 360 基因檢測 ⭐
- Quote：「就像拿到一份身體說明書，終於知道怎麼跟自己的身體相處，真的很安心。」
- Treatment：基因檢測｜Media：Reel
- Post：https://www.instagram.com/reel/C7q5gS3hT9Z/
- 身分：旅遊部落客｜Handle：**@bonbonelephant**（已確認）

### 2. Evelyn Chang 熏熏 — 360 基因檢測 ⭐
- Quote：「基因檢測報告幫助我更了解自己的身體，非常推薦大家有機會都要做一次。」
- Treatment：基因檢測・營養點滴｜Media：Post｜Doctor：Dr. Wilson
- Post：https://www.instagram.com/p/Cwjyy71Lrpi/
- 身分：旅遊／生活創作者（@evelynychang，現有大安頁也用她）

### 3. 蔡佩軒 Ariel Tsai — 過敏原檢測 ⭐（知名度高）
- Quote：「做了 224 項完整過敏原檢查，才知道原來我對這麼多東西過敏——而這些都讓身體發炎。」
- Treatment：過敏原檢測｜Media：Post｜Doctor：Dr. Mike 葉耀翔
- Post：https://www.instagram.com/p/C1USnW9S9-4/
- 身分：創作歌手（379K 粉絲）｜Handle：**@ariel_tsai**（已確認）

### 4. Taipei Foodie — 過敏原檢測（英文受眾）
- Quote：「快速抽完血兩週就拿到報告，醫師詳細說明，我才知道脹氣、疲勞、注意力不集中都可能是慢性過敏。」
- Treatment：過敏原檢測｜Media：Reel｜Doctor：Dr. Wilson
- Post：https://www.instagram.com/reel/CmeTxTwjPtT/
- 身分：美食 KOL（中英，156K 粉絲）｜Handle：**@taipeifoodie**（已確認）

### 5. 李瑜 Yu Lee — 基因檢測（2026 年度代言人）
- Quote：⚠️ 影片型，IG 字幕無法程式擷取 → 團隊手動補一句，或做成影片卡
- Treatment：基因檢測｜Media：Reel｜Doctor：Dr. Wilson
- Post：https://www.instagram.com/reel/DNf0u1fzAKY/
- 身分：作家・前《Tatler》台灣區總編輯・ĒSEN 2026 年度代言人（176K）｜Handle：**@yulee_yutopia**（已確認）

### 6. Elena & Patrick 陳柏勳 — 檢測・點滴（情侶，呼應 Superpower 的伴侶卡）
- Quote：⚠️ 影片型，需團隊手動補字幕或做影片卡
- Treatment：健檢・營養點滴｜Media：Reel｜Doctor：Dr. Wilson
- Post：https://www.instagram.com/reel/DQbuqXLkpIh/｜Profile：**@trailblazer.tw**（已確認）
- 身分：跨國伴侶創作者

### 7. Kurt 吳承暉 — 點滴・靜脈雷射
- Quote：⚠️ 需團隊補一句（Notion 內無圖文引言）
- Treatment：營養點滴・靜脈雷射｜Media：Post｜Doctor：Dr. Wilson
- Post：https://www.instagram.com/p/DSPV_fKEp8C/｜Handle：**@kurrrtwu**（已確認）

---

## C. Wall of Love — 完整名單（21 筆，皆附真實貼文連結）
直接匯入 CMS。引言已從原貼文擷取、修順。療程多元（基因/過敏原/點滴/PRP/健檢/減重）。

| Name | 療程 | 引言 Quote | Post URL | Media |
|---|---|---|---|---|
| 凡凡凡 | 基因檢測 | 能從檢測觀察到自己的獨特體質，提前注意和預防。 | instagram.com/p/CzWKK49ybWt/ | Post |
| 陳怡安 Angelina | 健檢・基因・點滴 | 明顯感受到疲累感降低，臉部與身體水腫也改善了。 | instagram.com/p/DAbE4IQzz7X/ | Post |
| Katy | 健檢・點滴 | 每次來 ĒSEN 都覺得心情很好。 | instagram.com/reel/CnTzV80I1Ln/ | Reel |
| 紫緹 JT | 過敏原檢測 | 遠離過敏原夠長的時間，身體的發炎反應都會消退。 | instagram.com/reel/CkQujBrgcdM/ | Reel |
| 林祐安 Sophia | 健檢 | 一個好診所，讓我更認識自己的身體狀況。 | instagram.com/p/CzYhPQDpkwD/ | Post |
| 家瑜 | PRP | 前額原本稀疏的頭髮，開始長出比較粗的髮束。 | instagram.com/p/C1WpPzhvyMQ/ | Post |
| 融融歷險記 | 基因檢測 | 追求健康平衡的人生，才是最大的財富。 | instagram.com/reel/C6bJ8QIuWo_/ | Reel |
| 慈飛 | 基因檢測 | 醫生說它像身體的指南，很像身體的 MBTI。 | instagram.com/p/CxPPZ_8PmWH/ | Post |
| Queena | 基因檢測 | 想從最源頭知道哪裡有問題，積極防範勝於治療。 | instagram.com/reel/C7B8nwtPAyc/ | Reel |
| KM | 健檢 | 確實幫我從「感覺」變成真的理解身體狀況。 | instagram.com/p/CziZh6mSqGG/ | Post |
| 陳韋丞 | PRP | 打完沒多久頭髮就變茂密，兩三週就有感。 | instagram.com/p/C371Bk8vHug/ | Post |
| Jojo | 過敏原檢測 | 不驗不知道、一驗嚇一跳，還好有檢測。 | instagram.com/reel/DCBuAcfyCoN/ | Reel |
| Ian | 健檢 | 吃了兩週保健品，身體明顯變得更有活力。 | instagram.com/p/CooUhZIBB2R/ | Post |
| Toby | 健檢 | 經過醫生仔細講解，怕病的我也能放心。 | instagram.com/p/Crg5k_USOfP/ | Post |
| Chacha | 健檢・點滴 | 打完點滴，從來沒這麼清醒過。 | instagram.com/p/Cs0EH9hreas/ | Post |
| Jeni | 健檢 | 怕抽血的我，在護理師耐心陪伴下緩解了緊張。 | instagram.com/reel/CoTaAmbg833/ | Reel |
| Emily | 基因檢測 | 與其等紅字出現再改變，不如主動提前預防。 | instagram.com/p/C6lMX1svvTi/ | Post |
| Lavande | 健檢 | 預防勝於治療，很老套，但絕對是真理。 | instagram.com/p/Cr2dovcuDok/ | Post |
| Angela | 健檢 | 真的就是有個關心你的家庭醫生的感覺。 | instagram.com/p/CoE4iycv6Cq/ | Post（@ness.wellness）|
| Grace | 基因檢測 | 清楚掌握身體的組成和現況，這種感覺好踏實。 | instagram.com/p/C9usgJSvj4O/ | Post |
| 小金魚 | 減重・ĒSEN CARE | 我穿得下五年前的衣服了！ | instagram.com/reel/DA3IRV-hN9-/ | Reel ⚠️ |

⚠️ 小金魚那則是從 **@esenmedical 官方帳號**發的個案推廣（引言是她本人的話，但貼文非她個人帳號）——用前確認。陳韋丞頁面另有一則 @dr.wilsontsou（院長，非本人），handle 留白。多數 KOL 個人 handle 未在貼文內明確標示，wall 卡片建議**連回貼文本身**即可（符合連回原文原則）。

**總量**：Featured 7（B 段）＋ Wall 21（本段）＝ **28 筆**，足夠開 carousel ＋ wall。資料庫還有更多，需要再擴。

## D. 數量與容器建議（最佳實務）
分兩種容器，量的策略不同：
- **Featured carousel（精選可點）**：curate **8–12 筆**最強的（引言好、療程多元、有名人）。使用者少滑超過前幾張，前段要精。
- **Wall of love（自動捲動牆，像 Superpower 那幾排）**：「**越多越好**」，**20–40＋**當 ambient 社會證明，每張連回原貼文。量大＝信任＋SEO＋廣度。
- 技術：wall 用「貼文截圖卡＋連回原文」，**不要嵌 40 個 IG iframe**（會拖慢頁面）。

## E. 狀態／提醒
- Handle：上面 7 筆**全部已確認**（含粉絲數）。
- 影片字幕：李瑜／Elena／Kurt 的 Reel 字幕**無法程式擷取**——團隊手動補一句，或做成影片卡。
- Wall：C 段 21 筆已備齊（含引言＋貼文連結）。需要再多可從資料庫續抓。
- 線框＋CMS 對應圖：見 `mockups/testimonial-section-wireframe.html`（PNG 可預覽）。
