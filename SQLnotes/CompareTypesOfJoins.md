# SQL 連接 (Joins) 筆記

SQL Join 用於根據多個表之間的共同欄位，將來自這些表的行組合起來。

---

## 1. 內連接 (Inner Joins)
`INNER JOIN` 傳回在多個表中**同時存在**且符合指定列匹配條件的行。

* **特性**：只有兩張表都有對應數據時，該列才會出現在結果中。
* **注意**：如果一個列同時存在於兩個表中，使用 `SELECT *` 時，該列會被傳回兩次。
* **範例**：
    ```sql
    SELECT username, operating_system, employees.device_id
    FROM employees
    INNER JOIN machines ON employees.device_id = machines.device_id;
    ```

---

## 2. 外連接 (Outer Joins)
`Outer Joins` 會擴展連接回傳的結果，即使另一張表沒有匹配的數據，也能保留部分表的原始記錄。

### A. 左外連接 (Left Joins)
`LEFT JOIN` 會傳回**第一個表（左表）中的所有記錄**，以及第二個表（右表）中符合指定列匹配條件的行。

* **特性**：如果右表沒有匹配項，結果中右表的相關欄位將顯示為 `NULL`。
* **範例**：
    ```sql
    SELECT *
    FROM employees
    LEFT JOIN machines ON employees.device_id = machines.device_id;
    ```

### B. 右外連接 (Right Joins)
`RIGHT JOIN` 與左連接相反，它會傳回**第二個表（右表）的所有記錄**，以及第一個表（左表）中符合匹配條件的行。

* **特性**：如果左表沒有匹配項，左表的欄位將顯示為 `NULL`。
* **範例**：
    ```sql
    SELECT *
    FROM employees
    RIGHT JOIN machines ON employees.device_id = machines.device_id;
    ```

### C. 全外連接 (Full Outer Joins)
`FULL OUTER JOIN` 傳回**兩個表中的所有記錄**。

* **特性**：您可以將其理解為完全合併兩個表的一種方式。只要其中一個表有匹配，就會顯示數據；若某一方缺乏匹配，則該方欄位以 `NULL` 填充。
* **範例**：
    ```sql
    SELECT *
    FROM employees
    FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
    ```

---

## 總結對比表

| 連接類型 | 傳回結果描述 |
| :--- | :--- |
| **Inner Join** | 僅傳回兩表皆有匹配的行 |
| **Left Join** | 傳回左表所有行 + 右表匹配行 |
| **Right Join** | 傳回右表所有行 + 左表匹配行 |
| **Full Outer Join** | 傳回左表與右表的所有行 |