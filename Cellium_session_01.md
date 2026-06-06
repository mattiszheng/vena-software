# Cellium 開發紀錄 — Session 01

> 日期：2026-05-05
> 結果：MVP v0.1 完成，initial commit `d2ea88a`

---

## 本次完成

### 功能
| 項目 | 狀態 |
|---|---|
| 2D 畫布（拖拉、縮放、平移） | ✅ React Flow |
| Markdown 編輯器（左寫右預覽） | ✅ |
| WikiLink `[[檔名]]` 自動生成連線 | ✅ |
| 本地檔案讀寫（Electron） | ✅ |
| 工作區概念 + 相對路徑 | ✅ |
| 工作區記憶（上次路徑自動載入） | ✅ |
| Light / Dark 主題切換 | ✅ |
| 語言切換（中文 / English） | ✅ i18n |
| Settings 面板（Ctrl+,） | ✅ |
| Inspector 右欄（檔案資訊 / 工作區統計） | ✅ |

### 技術架構
- **Scaffold**：electron-vite，react-ts 模板
- **Stack**：Electron + Vite + React 19 + TypeScript strict + Tailwind v4
- **Canvas**：reactflow v11
- **Markdown**：marked + DOMPurify
- **State**：Zustand（useWorkspaceStore / useSettingsStore）
- **Storage**：StorageProvider 抽象層，LocalStorageProvider 實作
- **關係存儲**：cellium.json 在 workspace 根目錄，不動原始 .md 檔

### 已知技巧
- shell 有 `ELECTRON_RUN_AS_NODE=1` 環境變數，用 `scripts/run.cjs` 在啟動前 delete 掉

---

## 未完成（PRD §7.1 剩餘）

| 項目 | 備註 |
|---|---|
| 手動連線 + 邊顏色/樣式 | PRD §4.5，核心差異化，建議優先 |
| 泛型節點（筆記 / 群） | PRD §4.1，需要資料模型重構 |
| 節點展開為子畫布 | PRD §4.3，UX 未拍板，最後做 |

---

## 下一步

**先用一週，記痛點，再決定做什麼。**

CC 建議順序：① 手動連線 + 邊樣式 → ② 泛型節點 + 筆記/群 → ③ 子畫布

---

## 產品方向補充（本次討論）

- **Zotero 整合方向**：不取代 Zotero，寄生在上面。把 workspace 指向 Zotero 本地資料夾，把文獻當節點讀進來，關係存在 cellium.json，完全不動 Zotero 檔案。
- **Word 銜接**：未來方向，MVP 後再評估。
- **開發語言**：PRD 留中文，build plan / code 留英文，CC 對話改繁體中文。
