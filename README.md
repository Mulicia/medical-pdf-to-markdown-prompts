# 生醫科研文獻高保真 Markdown 轉換與深度圖表解析專家規範
*(Biomedical Literature High-Fidelity Markdown & Scaffolding Expert Guidelines)*

這是一套專為大型語言模型（LLM / 多模態模型）設計的生醫學術文獻結構化轉換 Prompt 規範。旨在將 PDF 格式的生物醫學期刊文獻，高保真（High-Fidelity）地轉譯為結構清晰、數據精確的 Markdown 格式，並對複雜科學實驗圖表（Figures/Schemes）進行多模態深度解析。

---

## 📌 核心特色 (Key Features)

- **同行評審級高保真 (High Integrity):** 原文轉錄區杜絕未經指示的摘要與改寫，嚴格保留長段落、統計數值與原始語意。
- **圖表深度結構化 (Figure Scaffolding):** 告別單句圖表概括；針對長條圖、Western blot、流式細胞儀（FCM）、Kaplan–Meier 生存曲線、病理顯微切片等，進行分組定量、統計顯著性及機制路徑解構。
- **嚴謹證據邊界 (Evidence Fidelity):** 強制區分「原文轉錄」、「直接圖表數據」與「模型推論」，杜絕 AI 幻覺補造數值。
- **生醫命名法規 (Standardized Nomenclature):** 醫學、藥物與關鍵生化名詞一律採 `英文全名（中文，縮寫）` 格式呈現；菌名、基因與蛋白質遵循學術大小寫與斜體規範。
- **兩階段審核工作流 (Two-Phase Workflow):** 透過先掃描 OCR 與上下標疑點、待人工確認後再輸出的流程，確保文檔零瑕疵。

---

## 🔄 兩階段工作流程 (Workflow)

\`\`\`mermaid
flowchart LR
	A[上傳文獻 PDF] --> B[第一階段：校對與確認]
	B --> C{產出疑點對照表}
	C -->|使用者確認 / 回覆繼續| D[第二階段：格式化輸出]
	D --> E[高保真 Markdown 完整文件]

---
```text
├── README.md                                      # 專案說明文件
└── 醫學-pdf_to_markdown_expert_guidelines.md      # 核心專家規範 Prompt 主文件
```
