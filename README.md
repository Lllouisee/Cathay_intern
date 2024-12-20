# 新聞摘要
將兩篇新聞稿的內文輸入給 ChatGPT API，並請 ChatGPT 總結新聞稿內容
## 功能

### 新聞內容摘要
- 從提供的新聞網址抓取文章內容
- 使用 GPT-3.5-Turbo 模型生成結構化摘要，包括：
  - **主旨**：文章核心內容。
  - **重點**：包含關鍵數字、機構名稱和時間。
  - **詳述**：深入的具體細節描述。
- 需要有效的 OpenAI API 金鑰才能執行

## 備註
### 程式碼優化 - 圖片文字提取
- 利用 `pytesseract` 從文章中的圖片提取文字。
- 支援繁體中文文字（語言代碼：`chi_tra`）。
- 將提取的圖片文字合併到摘要中。

 如果圖片模糊或品質較低，文字提取可能失敗(如以上兩篇新聞內的圖片)。
