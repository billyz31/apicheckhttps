# Online Game Platform

一個基於現代 Web 技術構建的線上遊戲平台，包含完整的前後端分離架構與支付系統。

## 🛠 技術棧

### 前端 (Frontend)
- **框架**: Vue 3 (Composition API)
- **語言**: TypeScript
- **構建工具**: Vite
- **狀態管理**: Pinia
- **路由**: Vue Router
- **HTTP 客戶端**: Axios

### 後端 (Backend)
- **框架**: Laravel 11
- **語言**: PHP 8.2+
- **身份驗證**: Laravel Sanctum
- **資料庫**: PostgreSQL 15
- **Web 伺服器**: Nginx

### 基礎設施 (Infrastructure)
- **容器化**: Docker & Docker Compose
- **服務編排**:
  - `nginx`: 反向代理與靜態資源服務
  - `laravel`: 後端 API 服務
  - `postgres`: 資料庫服務

## 🚀 快速開始

### 前置要求
確保您的系統已安裝以下工具：
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### 安裝與運行

1. **克隆專案**
   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. **啟動服務**
   使用 Docker Compose 一鍵啟動所有服務：
   ```bash
   docker-compose up -d
   ```

3. **初始化設定** (首次運行)
   進入後端容器進行遷移與種子資料填充：
   ```bash
   docker-compose exec laravel php artisan migrate --seed
   ```

### 訪問服務

- **前端頁面**: [http://localhost](http://localhost)
- **後端 API**: [http://localhost:8000](http://localhost:8000)

## 📂 專案結構

```
.
├── backend/            # Laravel 後端源代碼
├── frontend/           # Vue 前端源代碼
├── docker-compose.yml  # Docker 服務定義
├── nginx.conf          # Nginx 配置
└── README.md           # 專案說明文件
```

## ✨ 功能特性

- **用戶系統**: 註冊、登入、個人資料管理
- **遊戲大廳**: 瀏覽可用遊戲
- **老虎機遊戲**: 模擬老虎機遊戲邏輯
- **錢包系統**: 存款、餘額查詢、交易記錄
- **系統診斷**: 自動化健康檢查與 API 測試

## 📝 開發說明

### 前端開發
```bash
cd frontend
npm install
npm run dev
```

### 後端開發
```bash
cd backend
composer install
php artisan serve
```

## ⚠️ 注意事項

- 本專案僅供學習與測試使用。
- 資料庫帳號密碼配置於 `.env` 與 `docker-compose.yml` 中。
