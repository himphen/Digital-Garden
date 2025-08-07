# Himphen's Blog

基於 Hugo 和 Congo 主題的個人部落格，使用 GitHub Actions 自動部署到 GitHub Pages。

## 🚀 功能特色

- ✅ 響應式設計，支援手機和桌面
- ✅ 深色/淺色主題自動切換
- ✅ 程式碼高亮和複製功能
- ✅ 文章搜尋功能
- ✅ 標籤和分類系統
- ✅ RSS 訂閱
- ✅ Google Analytics 整合
- ✅ 自動化部署

## 🛠️ 技術棧

- **Hugo**: 靜態網站生成器
- **Congo Theme**: 美觀的 Hugo 主題
- **GitHub Actions**: 自動化部署
- **GitHub Pages**: 免費託管
- **Markdown**: 內容格式

## 📦 本地開發

### 前置需求

- [Hugo Extended](https://gohugo.io/installation/) (推薦使用 Extended 版本)
- [Git](https://git-scm.com/)

### 安裝步驟

1. **克隆專案**
   ```bash
   git clone https://github.com/himphen/himphen-blog.git
   cd himphen-blog
   ```

2. **安裝主題**
   ```bash
   git submodule update --init --recursive
   ```

3. **本地測試**
   ```bash
   hugo server -D
   ```
   然後在瀏覽器開啟 http://localhost:1313

4. **建置網站**
   ```bash
   hugo
   ```

## 📝 寫作新文章

### 建立新文章
```bash
hugo new posts/my-new-post.md
```

### 文章 Front Matter 範例
```yaml
---
title: "文章標題"
description: "文章描述"
date: 2025-01-07
tags: ["標籤1", "標籤2"]
categories: ["分類"]
draft: false
---
```

### 文章內容
使用標準 Markdown 語法，支援：
- 標題、段落、列表
- 程式碼區塊
- 圖片和連結
- 表格
- 引用區塊

## 🎨 客製化

### 修改主題設定
編輯 `hugo.toml` 文件中的 `[params]` 部分。

### 自定義 CSS
編輯 `assets/css/custom.css` 文件。

### 添加新頁面
```bash
hugo new about/my-page.md
```

## 🚀 部署

### 自動部署
推送到 `main` 分支會自動觸發 GitHub Actions 部署。

### 手動部署
1. 在 GitHub 上建立新的 repository
2. 推送程式碼到 repository
3. 在 Settings > Pages 中啟用 GitHub Pages
4. 設定自定義域名 (可選)

## ⚙️ 配置

### Google Analytics
1. 在 Google Analytics 建立新的屬性
2. 複製追蹤 ID (格式: G-XXXXXXXXXX)
3. 在 `hugo.toml` 中更新 `googleAnalytics` 設定

### 自定義域名
1. 在 DNS 提供商設定 CNAME 記錄
2. 在 GitHub Pages 設定中添加自定義域名
3. 更新 `hugo.toml` 中的 `baseURL`

## 🔧 故障排除

### 常見問題

**Q: 主題無法載入**
A: 確認已正確安裝主題 submodule：
```bash
git submodule update --init --recursive
```

**Q: 本地建置失敗**
A: 檢查 Hugo 版本是否為 Extended 版本：
```bash
hugo version
```

**Q: 部署後樣式異常**
A: 確認 `hugo.toml` 中的 `theme = "congo"` 設定正確

**Q: 圖片無法顯示**
A: 將圖片放在 `static/` 目錄下，使用相對路徑引用

### 除錯技巧

1. **檢查 Hugo 版本**
   ```bash
   hugo version
   ```

2. **清理快取**
   ```bash
   hugo --gc
   ```

3. **詳細建置資訊**
   ```bash
   hugo --verbose
   ```

## 📁 專案結構

```
himphen-blog/
├── content/              # 文章內容
│   ├── posts/           # 部落格文章
│   ├── about/           # 關於頁面
│   └── _index.md        # 首頁內容
├── assets/              # 靜態資源
│   └── css/
│       └── custom.css   # 自定義樣式
├── static/              # 靜態文件
├── themes/              # 主題 (Congo)
├── hugo.toml            # Hugo 配置
├── .github/             # GitHub Actions
└── README.md            # 說明文件
```

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

## 📄 授權

MIT License

## 📞 聯絡

- **GitHub**: [@himphen](https://github.com/himphen)
- **Email**: himphen@example.com

---

*Happy Blogging! 🎉* 