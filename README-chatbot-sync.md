# ChatBot 與語意分析頁面同步說明

## 功能說明

現在 ChatBot 的用戶輸入會自動同步到 `semantic-analysis-demo.html` 頁面進行即時語意分析。

## 使用方式

### 1. 開啟主網站
```
http://localhost:5173/
```

### 2. 開啟語意分析測試頁面
在瀏覽器中開啟另一個分頁，直接打開：
```
file:///C:/Users/Sunnee.Pan/Desktop/learn/semantic-analysis-demo.html
```
或者在專案目錄中雙擊開啟 `semantic-analysis-demo.html`

### 3. 開始使用
1. 在主網站點擊右下角的「職涯領航員」圖示
2. 在 ChatBot 中輸入任何訊息，例如：
   - 「我失業了想學程式設計」
   - 「我在職想學烘焙」
   - 點擊任何快捷按鈕或選項

3. 切換到語意分析頁面，您會看到：
   - ✅ 輸入框自動填入您的訊息
   - ✅ 即時分析結果顯示
   - ✅ 使用者檔案 JSON 更新

## 同步內容

以下 ChatBot 互動會自動同步：
- ✅ 手動輸入的文字
- ✅ 點擊的選項（如「職前」、「在職」）
- ✅ 快捷按鈕（如「找職前課程」、「熱門課程」）
- ✅ FAQ 按鈕（如「補助說明」、「上課時間」）

## 技術實作

使用 `localStorage` 進行跨頁面通訊：
- **儲存鍵**：`chatbot-user-input`
- **時間戳**：`chatbot-timestamp`

## 變更記錄

### semantic-analysis-demo.html
- ❌ 刪除所有測試案例資料
- ✅ 新增 localStorage 監聽器
- ✅ 新增「即時同步 ChatBot 對話」提示
- ✅ 自動接收並分析 ChatBot 輸入

### src/components/ChatBot.jsx
- ✅ `handleSend()` - 同步手動輸入
- ✅ `handleOptionClick()` - 同步選項點擊
- ✅ `handleShortcut()` - 同步快捷按鈕
  - popular - 熱門課程
  - quick_search - 快速查詢
  - faq - 常見問題

## 注意事項

1. **兩個頁面需要在同一瀏覽器中開啟**才能同步
2. **localStorage 限制**：如果頁面協議不同（http vs file://），可能無法同步
3. 建議同時開啟兩個分頁以觀察即時同步效果

## 除錯方式

如果同步沒有生效，請檢查：
1. 瀏覽器控制台是否有錯誤訊息
2. 在控制台輸入以下指令檢查 localStorage：
   ```javascript
   localStorage.getItem('chatbot-user-input')
   ```
3. 確認兩個頁面都已正確載入

## 範例流程

```
用戶在 ChatBot 輸入：
「我失業了想學程式設計」

↓ (自動同步)

語意分析頁面顯示：
【就業狀態】待業中 (99%)
【職業背景】資訊科技 (95%)
【建議訓練類型】職前訓練
```

## 未來優化

- [ ] 支援雙向同步（語意分析頁面 → ChatBot）
- [ ] 新增同步歷史記錄
- [ ] 支援跨瀏覽器同步（使用 WebSocket）

