# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 专案结构

Monorepo-style 工作簿，每个子专案放在独立目录：

```
Green-Diva-Workbook/
├── 01-Japan-Invoice-Scanner/   # FastAPI 发票 OCR 服务（独立仓库：CongoKim/01-Japan-Invoice-Scanner）
└── NN-Project-Name/            # 未来子专案（两位数编号 + PascalCase）
```

每个子专案须包含 `README.md`、`.env.example` 与 `CLAUDE.md`。

## Git 规范

Commit 格式：`<type>(<scope>): <描述>`

- type：`feat` / `fix` / `refactor` / `docs` / `chore` / `test`
- scope：子专案简称，如 `japan-invoice`、`budget-tracker`
- 分支：`main`（稳定）、`feat/<scope>/<description>`（功能开发）

## 注意

各子专案均为独立 Git 仓库，主目录不追踪子专案文件。子专案架构细节见各自的 `CLAUDE.md`。

## 语言

所有回复使用**简体中文**。
