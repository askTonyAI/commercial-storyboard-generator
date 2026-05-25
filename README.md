# Commercial Storyboard Generator

一個用來快速生成商業廣告分鏡板的 ChatGPT / Codex Skill。

它會把品牌、產品、受眾、痛點、期待轉變、調性與主標題整理成一套可執行的廣告分鏡流程，輸出 16:9 的商業 storyboard board 規劃，包含 Key Visual、10 格分鏡、產品收尾與最終英文圖像生成 prompt。

這個 skill 的目的不是取代行銷判斷，而是把「從 brief 到可參考分鏡」這段流程變快。

AI 可以幫你生成分鏡，但它不會自動知道你到底該解決什麼問題。它可以排出 10 格故事，但 consumer insight 是否有力、產品出場是否自然、轉換是否真的能說服人，仍然需要由人負責。

## 適合用在什麼情境

- 商業廣告分鏡發想
- 產品廣告 storyboard
- Campaign board
- 社群短影音分鏡
- Key Visual 加 10 格分鏡版面
- 一頁式 16:9 廣告提案圖
- ChatGPT Images / GPT Images 的商業分鏡 prompt
- 從產品 brief 快速產出可討論的視覺提案

## 它會產出什麼

這個 skill 預設會產出：

1. Creative strategy
2. Key idea
3. Before / Trigger / After 的敘事轉換
4. 一張 16:9 storyboard board 的版面規劃
5. TOP：主視覺 Key Visual
6. MIDDLE：10 格分鏡
7. BOTTOM：產品 packshot、品牌與 tagline
8. 最終英文 image-generation prompt

如果你明確要求產圖，它會再進一步生成一張完整的 16:9 商業分鏡圖。

## 使用前需要準備的 8 個欄位

這個 skill 有一個核心規則：缺少關鍵 brief 時，不會硬編。

你需要提供：

1. 品牌
2. 產品
3. 目標受眾
4. 消費者問題
5. 期待轉變
6. 調性
7. 圖中文字語言
8. 版面主標題 / 主 headline

如果缺少其中任何一項，skill 會先請你補齊，不會直接進入分鏡或 prompt 生成。

## 使用範例

```text
請用 commercial-storyboard-generator 幫我做一張 16:9 商業廣告分鏡板。

品牌：寶礦力水得
產品：寶礦力水得 500ml
目標受眾：夏天通勤、運動後容易疲憊的上班族
消費者問題：流汗後身體缺水，精神變差
期待轉變：喝下後恢復清爽、專注、有活力
調性：清新、陽光、日系、真實生活感
圖中文字語言：繁體中文
版面主標題：補回流失的清爽

請輸出 creative strategy、10 格分鏡，以及最終 image prompt。
```

如果想直接生成圖片，可以加上：

```text
最後請生成一張 16:9 storyboard 圖。
```

## 安裝方式

把整個資料夾放到 Codex skills 目錄：

```text
~/.codex/skills/commercial-storyboard-generator
```

資料夾內需要包含：

```text
commercial-storyboard-generator/
  SKILL.md
  agents/
  assets/
  references/
```

安裝後，只要用自然語言提出商業分鏡、廣告 storyboard、campaign board、產品視覺提案等需求，Codex 就可以自動使用這個 skill。

## 設計原則

這個 skill 會強制檢查 brief，避免模型在最重要的策略欄位上自行腦補。

它特別重視：

- 產品必須是轉變的觸發點，而不是畫面裡的被動道具
- 故事要從問題走向使用，再走向轉變與 payoff
- 10 格分鏡不能只是漂亮畫面拼貼
- Key Visual、分鏡與產品收尾要形成同一個銷售邏輯
- 最終 prompt 以英文撰寫，但圖中文字遵照使用者指定語言

## 重要提醒

這個 skill 可以讓產出變快，但不會讓判斷自動變準。

它適合用來快速做第一輪提案、課程示範、廣告概念發想與視覺 prompt 草稿。不過真正決定作品能不能賣、能不能打中受眾的，仍然是 brief 品質、consumer insight、產品定位與銷售判斷。

換句話說，它能幫你更快看到一個方向，但不會替你保證那個方向值得做。

