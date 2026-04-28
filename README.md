# 🛡️ Cybersecurity Learning Journey: Linux & SQL Essentials

這是我從零開始轉職資安工程師的學習紀錄。我堅持從**第一原理 (First Principles)** 出發，不只是死背指令，而是理解技術背後的運作邏輯。

---

## 📑 目錄
* [Linux 系統管理](#-linux-系統管理)
* [SQL 資料庫與日誌分析](#-sql-資料庫與日誌分析)
* [核心術語表](#-核心術語表)
* [學習方法論](#-學習方法論)

---

## 🐧 Linux 系統管理
在 Linux 環境中，我學習如何透過指令列（CLI）與作業系統溝通，這是進入 SOC 運維與滲透測試的基礎。

### 核心概念
* **環境存取**：利用 `sqlite3` 等工具在 Linux 中直接操作資料庫。
* **資料過濾**：掌握 `grep`、`find`、`sed` 與 `cut` 等強大工具處理系統檔案。
* **系統架構**：理解 Linux 將資料視為「純文字流」的自由特性，對比 SQL 的嚴謹結構。

> **實作紀錄**：已成功實作 Windows 環境遠端連接至 Ubuntu VM，並進行基礎 CLI 管理。

---

## 🗄️ SQL 資料庫與日誌分析
針對資安分析（SOC Analyst）需求，我專注於如何使用 SQL 從大量日誌中篩選出潛在威脅。

### 1. 邏輯運算與篩選
* 使用 `AND`、`OR`、`NOT` 進行精確條件過濾。
* 掌握 `<>` 與 `!=` 的否定邏輯應用。

### 2. 資料表連接 (Joins)
為了分析關聯事件，我學習了多種 Join 技術：
* **Inner Join**：提取兩表匹配的精確資料。
* **Outer Join (Left/Right/Full)**：確保在資料不完全匹配時，仍能保留關鍵的審計紀錄。

### 3. 聚合函數 (Aggregation)
* 利用 `COUNT()`、`AVG()`、`SUM()` 進行流量統計與異常頻率分析。

---

## 📖 核心術語表
| 術語 | 關鍵定義 |
| :--- | :--- |
| **主鍵 (Primary Key)** | 每一行的唯一識別身分。 |
| **外鍵 (Foreign Key)** | 建立表與表之間關聯的橋樑。 |
| **通配符 (Wildcard)** | SQL 靈魂，用於模糊搜尋（如 `%`）。 |
| **關係型資料庫** | 透過關聯表組成的結構化數據系統。 |

---

## 🧠 學習方法論：第一原理 (First Principles)
我不滿足於「如何做 (How)」，更追求「為什麼 (Why)」。
* **拆解複雜性**：將資安架構拆解為最基礎的網路協議與運算邏輯。
* **專案驅動**：目前正在開發 **Python 虛擬貨幣監控機器人**，實踐 API 調用與自動化腳本撰寫。
* **持續進階**：目前專攻 SQL 模式匹配（LIKE/WHERE）在 Log 搜索中的實際應用。

---

## 📈 未來目標
- [ ] 深入學習 Python Web Scraping 與自動化工具。
- [ ] 實踐更複雜的網路封包分析 (Scapy / Wireshark)。
- [ ] 申請 Taichung 地區之 entry-level SOC Analyst 職位。

---
**Wu Zheng Liang** *Cybersecurity Enthusiast | Career Changer | Python Learner*
