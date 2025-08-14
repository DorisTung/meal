# 亞東美食沙漠之今天吃什麼

智能餐廳選擇系統，結合天氣資訊與個人偏好。

## 功能特色

- 🍽️ 智能餐廳選擇
- 🌤️ 即時天氣資訊整合
- 🎨 雙主題設計 (Mario / Synology)
- 📊 歷史記錄管理
- 🏪 餐廳資料管理
- 📱 響應式設計

## 技術棧

- **前端**: Next.js 15, React, TypeScript
- **UI 框架**: Shadcn UI, Tailwind CSS
- **資料庫**: Prisma ORM, SQLite

## 本地開發

### 環境需求
- Node.js 18+
- npm 或 pnpm

### 安裝步驟

1. 克隆專案
```bash
git clone <repository-url>
cd meal-selection-app
```

2. 安裝依賴
```bash
npm install
```

3. 設定環境變數
```bash
cp .env.example .env.local
```

4. 初始化資料庫
```bash
npx prisma generate
npx prisma db push
```

5. 啟動開發伺服器
```bash
npm run dev
```

6. 開啟瀏覽器訪問 [http://localhost:3000](http://localhost:3000)

## 部署到生產環境

### 使用 Railway (推薦)

1. **準備部署**
   - 確保所有程式碼已提交到 Git
   - 檢查 `package.json` 中的腳本是否正確

2. **部署步驟**
   ```bash
   # 連接 GitHub 倉庫
   # 選擇 Node.js 環境
   # 設定環境變數
   # 自動部署
   ```

### 使用其他平台

#### Netlify
1. 連接 Git 倉庫
2. 設定建置命令: `npm run build`
3. 設定發布目錄: `.next`
4. 設定環境變數

#### Vercel
1. 安裝 Vercel CLI: `npm i -g vercel`
2. 登入: `vercel login`
3. 部署: `vercel`

## 資料庫設定

### 本地開發
- 使用 SQLite 資料庫
- 資料庫檔案: `prisma/dev.db`

### 生產環境
- 建議使用 Railway Postgres 或其他 PostgreSQL 服務
- 設定 `DATABASE_URL` 環境變數

## 環境變數

```env
# 資料庫連接
DATABASE_URL="file:./dev.db"

# 天氣 API (可選)
WEATHER_API_KEY="your-api-key"
```

## 專案結構

```
meal-selection-app/
├── app/                 # Next.js App Router
│   ├── api/            # API 路由
│   ├── globals.css     # 全域樣式
│   ├── layout.tsx      # 根佈局
│   └── page.tsx        # 首頁
├── components/         # React 元件
├── lib/               # 工具函數
├── prisma/            # 資料庫 schema
└── public/            # 靜態資源
```

## 貢獻指南

1. Fork 專案
2. 建立功能分支
3. 提交變更
4. 發起 Pull Request

## 授權

MIT License

## 支援

如有問題或建議，請開啟 Issue 或聯繫開發者。
