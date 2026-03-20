# Green-Diva Workbook

## 專案結構

這是一個多子專案的工作簿（monorepo-style）。每個子專案放在獨立的子目錄中。

```
Green-Diva-Workbook/
├── 01-Japan-Invoice-Scanner/   # 子專案 01
├── 02-Next-Project/            # 子專案 02（未來）
└── ...
```

### 命名規則

- 子目錄格式：`NN-Project-Name`（兩位數編號 + 連字號 + PascalCase 名稱）
- 例：`01-Japan-Invoice-Scanner`、`02-Budget-Tracker`

## Git 規範

### Commit 訊息格式

```
<type>(<scope>): <簡短描述>

<選填：詳細說明>
```

**type 類型：**
- `feat` — 新功能
- `fix` — 修復 bug
- `refactor` — 重構（不改變行為）
- `docs` — 文件更新
- `chore` — 雜務（依賴更新、設定等）
- `test` — 測試相關

**scope**：子專案名稱，例如 `japan-invoice`、`budget-tracker`

**範例：**
```
feat(japan-invoice): 新增 PDF 發票解析功能
fix(japan-invoice): 修正日期格式解析錯誤
chore: 更新 .gitignore
```

### 分支策略

- `main` — 穩定版本，各子專案的可運行狀態
- `feat/<scope>/<description>` — 功能開發分支

## 子專案規範

每個子專案應包含：
- `README.md` — 說明用途、安裝方式、使用方式
- `.env.example` — 環境變數範例（不 commit 實際 `.env`）

## 語言

所有回复使用**简体中文**。
