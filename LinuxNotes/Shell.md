# Linux Shell 基礎筆記

## 🖥️ 什麼是 Shell？


* **定義：** Shell 是一款 **命令列解釋器 (Command Line Interpreter)**。
* **運作邏輯：**
    1. **接收：** 接收使用者輸入的指令。
    2. **解釋：** 執行內部程序來解釋這些指令。
    3. **傳遞：** 將解釋後的指令傳送給 **內核 (Kernel)**。
    4. **回傳：** 處理完畢後，將結果傳回給使用者。

---

## 🐚 Shell 的常見類型 (Types of Shells)

目前 Linux 與 Unix 系統中存在多種不同的 Shell 實作，常見的包括：

* **Bourne-Again Shell (bash)**
    * 這是目前大多數 Linux 發行版中的 **預設 shell**。
* **Z Shell (zsh)**
    * 擁有強大的外掛支援（如 Oh My Zsh）與自動補全功能，是許多開發者的首選。
* **C Shell (csh)**
    * 語法結構類似於 C 語言。
* **Enhanced C shell (tcsh)**
    * C shell 的增強版本，具備指令補全與編輯功能。
* **Korn Shell (ksh)**
    * 結合了 Bourne shell 與 C shell 的特性，主要用於某些商業型 Unix 系統。