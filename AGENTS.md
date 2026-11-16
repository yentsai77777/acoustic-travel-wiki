# AGENTS.md — 臺灣史料轉譯與三天兩夜走讀知識庫 (HistoriTrip Wiki)

> **給 AI Agent 的首要指令**：每次收到「新增史料走讀主題」或「修改網頁」的任務前，請務必先完整閱讀本文件。所有檔案命名、HTML 卡片結構、景點對應邏輯與三天兩夜行程格式，皆須 100% 遵守本手冊規範，切勿自行猜測或破壞既有版面。

---

## 1. 專案目的 (Project Purpose)
本專案採用 **Karpathy LLM Wiki 模式**，旨在建立一個能將「生硬的臺灣歷史文獻或事件筆記」自動轉譯為「具文化深度的歷史景點介紹與三天兩夜走讀行程」的靜態知識庫網站（由政大蔡秉言維護）。
使用者只需將蒐集到的歷史文本或事件摘要放入 `raw/` 資料夾，AI Agent 即可依本規範自動提煉史料重點、匹配對應的實體歷史場域，並規劃出結構一致的「三天兩夜（3 Days 2 Nights）走讀路線」展示於網站上。

---

## 2. 資料夾與檔案命名結構 (Directory & File Naming Rules)
本專案維持簡潔的三層式資料流（`raw/` 史料輸入 ➔ `index.html` 走讀卡片展示 ➔ `log.md` 變更紀錄）：

```text
project-root/
├── AGENTS.md                 # AI 員工手冊（本規範檔，AI 不可擅自刪除或覆寫規則）
├── README.md                 # GitHub 專案說明檔
├── log.md                    # AI 每次新增或修改主題後的執行紀錄
├── index.html                # 網站首頁（收錄所有史料走讀卡片與三天兩夜行程抽屜）
└── raw/                      # 【史料輸入區】存放原始歷史文獻、事件摘要或讀書筆記 (.md)
    ├── raw-01-taipei-tea-dadaocheng.md
    ├── raw-02-white-terror-jingmei-greenisland.md
    └── raw-03-tainan-maritime-trade.md
