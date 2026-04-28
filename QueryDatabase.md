# 📊 SQL 基礎查詢筆記

在資料庫的世界裡，SQL 查詢就像是向資料庫發問。所有的查詢都建立在兩個核心關鍵字之上：`SELECT` 與 `FROM`。

---

## 1. 核心關鍵字 (Core Keywords)

### SELECT 
* **功能**：指示資料庫要「傳回哪些欄位（Columns）」。
* **用法**：
    * **選擇特定欄位**：`SELECT 欄位A, 欄位B` (使用逗號分隔)。
    * **選擇所有欄位**：`SELECT *` (星號 `*` 代表表格中的所有列)。

### FROM
* **功能**：指定要查詢的「表格名稱（Table）」。
* **用法**：`FROM 表格名稱`。

> **注意：** 在 SQL 語句的最後必須加上 **分號 ( ; )**，這代表指令的結束。

---

## 2. 排序資料 (Sorting Data)

### ORDER BY
* **功能**：根據指定的一個或多個欄位對回傳的記錄進行排序。
* **排序方式**：
    * **升序 (預設)**：由小到大排序。
    * **降序 (DESC)**：在欄位後方加上 `DESC` 關鍵字，改為由大到小排序。

---

## 💡 綜合範例 (SQL Query Example)

假設你有一個名為 `employees` 的員工表格，你想查看所有員工的姓名（name）和薪水（salary），並按照薪水**由高到低**排列：

```sql
SELECT name, salary
FROM employees
ORDER BY salary DESC;