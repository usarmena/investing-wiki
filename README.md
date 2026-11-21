# 📚 FinWiki：個人理財與指數化投資入門（LLM Wiki × 教學 HTML 簡報）

本專案以「先討論、後生成」方式建構 5 篇結構化 LLM Wiki 知識庫，並透過雙重檢查迴圈（Double-Loop Graph）將專業理財知識轉譯為 9 頁零基礎易懂的互動式教學 HTML 簡報。

## 🔗 線上瀏覽連結
- **LLM Wiki 知識庫首頁**：https://usarmena.github.io/investing-wiki/
- **9 頁互動教學 HTML 簡報**：https://usarmena.github.io/investing-wiki/slides.html
- **專案開發規範**：[`AGENTS.md`](./AGENTS.md)

## 🔄 Workflow / Loop Graph 流程圖

```mermaid
flowchart LR
    A["Step 1<br/>收集理財資料"] --> B["Step 2<br/>整理 5 篇 Wiki"]
    B --> C{"Gate 1<br/>公式與事實檢查"}
    C -- "退回修正" --> B
    C -- "通過" --> D["Step 3<br/>規劃白話簡報大綱"]
    D --> E{"Gate 2-A<br/>易懂度與邊界檢查"}
    E -- "退回重寫" --> D
    E -- "通過" --> F["Step 4<br/>生成 9 頁 HTML 簡報"]
    F --> G{"Gate 2-B<br/>排版與來源檢查"}
    G -- "退回調整" --> F
    G -- "通過" --> H["Step 5<br/>部署 GitHub Pages"]
```