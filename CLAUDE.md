# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 专案结构

Monorepo-style 工作簿，每个子专案放在独立目录，命名格式 `NN-Project-Name`（两位数编号 + PascalCase）。每个子专案须包含 `README.md`、`.env.example` 与 `CLAUDE.md`。

各子专案均为独立 Git 仓库，主目录通过 `.gitignore` 的 `[0-9][0-9]-*/` 模式排除所有子专案文件。因此在主目录执行 `git status` 不会显示子专案的变更；需 `cd` 进入子专案目录操作其 Git。子专案架构细节见各自的 `CLAUDE.md`。

当前子专案：
- `01-Japan-Invoice-Scanner/` — FastAPI 发票 OCR 服务，多 AI 模型交叉验证（独立仓库：CongoKim/01-Japan-Invoice-Scanner）

## 开发命令

### 01-Japan-Invoice-Scanner

```bash
cd 01-Japan-Invoice-Scanner
cp .env.example .env               # 填写 GEMINI_API_KEY、OPENAI_API_KEY、ANTHROPIC_API_KEY
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000   # 前端 SPA + API 同端口
```

测试：

```bash
cd 01-Japan-Invoice-Scanner
pytest                              # 运行全部测试
pytest tests/test_invoice_amounts.py  # 运行单个测试文件
pytest -k "test_name"               # 按名称筛选测试
```

## Git 规范

Commit 格式：`<type>(<scope>): <描述>`

- type：`feat` / `fix` / `refactor` / `docs` / `chore` / `test`
- scope：子专案简称，如 `japan-invoice`、`budget-tracker`
- 分支：`main`（稳定）、`feat/<scope>/<description>`（功能开发）

## 语言

所有回复使用**简体中文**。
