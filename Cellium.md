# Cellium

Better Finder / Explorer:用 2D 空間取代資料夾的視覺化檔案整理層。本地優先、開源、不鎖定使用者。Vena Software 旗下產品。

對標關係:Notion 之於 Word / Notepad——不取代 Finder,是「第三種使用檔案的方式」。

## 規格 source of truth

PRD 在 repo,不在這份 vault:

```
C:\Users\Mattis\Documents\Projects\claude_cellium\PRD.md
```

當前版本 v0.5(2026-05-15),產品定位從 v0.4 的「graph-first 多模態知識編輯器」轉向「better Finder」。

## 當前階段

- **v0.1 已完成**(2026-05-05,initial commit `d2ea88a`):React Flow 2D 畫布、Markdown 編輯器、WikiLink、Electron 本地檔案、工作區、主題/i18n、Settings、Inspector、StorageProvider + LocalStorageProvider、cellium.json。詳見 [[Cellium_session_01]]。
- **v0.5 MVP 剩餘**(repo PRD §7.2):多模態節點(icon + 雙擊開檔)、拖檔進畫布、自由排佈、範本系統、Onboarding;之後再做手動連線/邊樣式、泛型節點、子畫布。
- **MVP 完成判準**(repo PRD §7.4):自己用會不會痛 + 找 3-5 個非技術朋友試用驗證「桌面亂痛點普遍」。

## 商業模式

跟 Cumulus 走不同邏輯:Cumulus 是 SaaS 訂閱(Notion 模式),Cellium 是 Obsidian 模式——本地永遠免費,五個付費點(commercial license / app store 買斷 / AI 雲端推論 / 多人協作 / Cellium 官方 Sync)。詳見 repo PRD §五。

域名 `cellium.app` 已購入(2026-05-05)。

## 相關紀錄

- [[Cellium_naming_journey]] — Cellium 命名歷程
- [[Cellium_session_01]] — v0.1 開發 session 紀錄

## Vena 視角

(待補)
