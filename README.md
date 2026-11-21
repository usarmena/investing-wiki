# 📚 FinWiki：個人理財與指數化投資入門（LLM Wiki × 教學 HTML 簡報）

本專案以「先討論、後生成」方式建構 5 篇結構化 LLM Wiki 知識庫，並透過雙重檢查迴圈（Double-Loop Graph）將專業理財知識轉譯為 9 頁零基礎易懂的互動式教學 HTML 簡報。

## 🔗 線上瀏覽連結
- **LLM Wiki 知識庫首頁**：https://usarmena.github.io/investing-wiki/
- **9 頁互動教學 HTML 簡報**：https://usarmena.github.io/investing-wiki/slides.html
- **專案開發規範**：[`AGENTS.md`](./AGENTS.md)

## 🔄 Workflow / Loop Graph 流程圖

```mermaid
flowchart TD
    A["Step 1：收集理財核心資料"] --> B["Step 2：Ingest 整理 5 篇 LLM Wiki (.md)"]
    B --> C{"Gate 1：Wiki 事實與公式檢查"}
    C -- "FAIL：公式或數據有誤" --> B
    C -- "PASS" --> D["Step 3：查詢 Wiki 規劃白話簡報大綱 (1頁1概念＋生活類比)"]
    D --> E{"Gate 2-A：大綱易懂度與邊界檢查"}
    E -- "FAIL：超綱或內容過載" --> D
    E -- "PASS" --> F["Step 4：生成 9 頁互動式教學 HTML 簡報"]
    F --> G{"Gate 2-B：排版與來源對應檢查"}
    G -- "FAIL：破版或漏來源" --> F
    G -- "PASS" --> H["Step 5：部署至 GitHub Pages 上線"]
```