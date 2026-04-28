# 👥 Linux 系統管理：使用者與權限控制

## 🔑 超級使用者權限 (Privilege Escalation)
* **`sudo` (Super User Do)**：
    * **功能**：暫時授予普通使用者更高的執行權限（通常是 Root 權限）。
    * **核心概念**：遵循「最小權限原則」，平時使用一般帳號，僅在需要系統變更時才使用 `sudo`。

---

## 🧑‍💻 使用者帳號管理 (User Management)

### 1. 新增使用者：`useradd`
用於在系統中建立新帳號。
* **常用選項**：
    * `-g`：設定使用者的**主要群組 (Primary Group)**。
    * `-G`：將使用者加入**次要群組 (Supplementary Groups)**。
* **範例**：`sudo useradd -g users -G security,admin zhengliang`

### 2. 修改使用者：`usermod`
用於調整現有帳號的設定。
* **常用選項**：
    * `-d`：更改使用者的**家目錄 (Home Directory)** 路徑。
    * `-l`：更改使用者的**登入名稱 (Login name)**。
    * `-L`：**鎖定帳戶 (Lock)**，使該使用者暫時無法登入系統。

### 3. 刪除使用者：`userdel`
* **基本指令**：`userdel [使用者名稱]`
* **完整刪除**：`-r` 選項。
    * 如果不加 `-r`，系統僅刪除帳號，會保留該使用者的家目錄檔案。
    * 使用 `userdel -r` 會連同主目錄與檔案一併清除。

---

## 🏷️ 所有權管理 (Ownership)
* **`chown` (Change Owner)**：
    * **功能**：更改檔案或目錄的所有權。
    * **語法**：`sudo chown [使用者]:[群組] [檔案名稱]`
    * **範例**：`sudo chown analyst:security report.txt` (將檔案擁有者改為 analyst，群組改為 security)。
