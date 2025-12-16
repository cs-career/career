# 職業訓練整合網 PRO

這是一個使用 React 構建的職業訓練課程查詢平台，提供課程搜尋、篩選和智能聊天機器人服務。

## 技術棧

- **React 18** - UI 框架
- **Vite** - 構建工具
- **Tailwind CSS** - 樣式框架
- **Lucide React** - 圖標庫

## 專案結構

```
職訓智慧小幫手/
├── src/
│   ├── components/
│   │   └── ChatBot.jsx      # 聊天機器人組件
│   ├── data/
│   │   └── courses.js       # 課程資料
│   ├── utils/
│   │   └── filterCourses.js # 課程篩選工具函數
│   ├── App.jsx              # 主應用組件
│   ├── main.jsx             # 應用入口
│   └── index.css            # 全局樣式
├── index.html               # HTML 模板
├── package.json             # 專案配置
├── vite.config.js          # Vite 配置
├── tailwind.config.js      # Tailwind 配置
└── postcss.config.js       # PostCSS 配置
```

## 安裝與運行

### 1. 安裝依賴

```bash
npm install
```

### 2. 啟動開發伺服器

```bash
npm run dev
```

開發伺服器將在 `http://localhost:5173` 啟動。

### 3. 構建生產版本

```bash
npm run build
```

### 4. 預覽生產版本

```bash
npm run preview
```

## 功能特色

- ✅ 課程搜尋與篩選
- ✅ 職前/在職訓練分類
- ✅ 智能聊天機器人（職涯領航員）
- ✅ 響應式設計
- ✅ 現代化 UI/UX

## 組件說明

### App.jsx
主應用組件，包含：
- 導航欄
- Hero 區域（搜尋功能）
- 課程列表展示
- 頁腳

### ChatBot.jsx
智能聊天機器人組件，提供：
- 互動式對話介面
- 課程推薦功能
- 多步驟問卷流程

## 開發說明

專案使用 Vite 作為構建工具，支援：
- 快速熱模組替換 (HMR)
- ES6+ 語法支援
- 自動 CSS 處理

## 瀏覽器支援

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

