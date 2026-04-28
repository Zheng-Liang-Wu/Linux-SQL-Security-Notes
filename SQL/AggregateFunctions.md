# SQL 聚合函數 (Aggregate Functions)

聚合函數是對一組資料點進行計算，並將多個值縮減（或轉換）為一個**單一計算結果**的函數。這在製作數據統計報告時非常有用。

---

## 常用聚合函數

### 1. COUNT 函數
`COUNT()` 會傳回一個數字，表示符合查詢條件的**行數（Row count）**。

* **用途**：計算記錄的數量。
* **範例**：
    ```sql
    -- 計算員工總人數
    SELECT COUNT(*) FROM employees;

    -- 計算有填寫電子郵件的員工數量 (會忽略 NULL 值)
    SELECT COUNT(email) FROM employees;
    ```

### 2. AVG 函數
`AVG()` 傳回一列數值資料中的**平均值**。

* **用途**：計算特定欄位的平均數。
* **範例**：
    ```sql
    -- 計算所有員工的平均薪資
    SELECT AVG(salary) FROM employees;
    ```

### 3. SUM 函數
`SUM()` 傳回一列數值資料中的**總和**。

* **用途**：計算特定欄位的加總數值。
* **範例**：
    ```sql
    -- 計算該年度部門的總預算支出
    SELECT SUM(budget) FROM departments;
    ```

