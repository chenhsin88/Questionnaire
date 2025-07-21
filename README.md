# Questionnaire 問卷調查系統

本專案為動態問卷系統，使用 Angular 17 製作前端、Spring Boot 開發後端，並搭配 MySQL 資料庫儲存問卷、題目與填答資料。  
本系統支援問卷建立、題型管理、使用者填寫與圖表化統計結果，適合應用於意見調查、學習測驗、行銷調研等場景。

---

## 🧩 功能特色

### 🔹 前台（使用者端）

- 填寫問卷、預覽送出
- 題型支援：單選、多選、簡答
- 統計圖表顯示結果（Chart.js）

### 🔸 後台（管理者端）

- 建立 / 編輯 / 刪除問卷
- 管理題目與作答紀錄
- 圖表顯示填答統計結果
- 可控問卷是否公開

---

## 🛠️ 使用技術

### 🔹 前端 Frontend

- Angular 17
- TypeScript / SCSS / HTML
- Chart.js
- Angular Material

### 🔸 後端 Backend

- Spring Boot (Java)
- MySQL 8
- Spring Data JPA (Hibernate)
- RESTful API

---

## 🚀 快速開始（後端）

1. 建立 MySQL 資料庫：

   ```sql
   CREATE DATABASE quiz14 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```

2. 匯入建表與假資料：

   - 將 `schema.sql` 和 `data.sql` 放入 `src/main/resources/`
   - 使用 MySQL Workbench 或 CLI 匯入也可以

3. 修改 `src/main/resources/application.yml`：

   ```yaml
   spring:
     datasource:
       url: jdbc:mysql://localhost:3306/quiz14
       username: root
       password: yourpassword
     jpa:
       hibernate:
         ddl-auto: none
       show-sql: true
   ```

4. 啟動 Spring Boot 專案：

   ```bash
   ./mvnw spring-boot:run
   ```

---

## 🚀 快速開始（前端）

1. 進入前端專案資料夾：

   ```bash
   cd frontend
   ```

2. 安裝套件（含 Chart.js 與 Angular Material）：

   ```bash
   npm install
   npm install chart.js
   ng add @angular/material
   ```

3. 啟動 Angular 專案：

   ```bash
   ng serve
   ```

4. 預設網址：

   ```
   http://localhost:4200
   ```

---

## 📁 專案結構說明

| 資料夾 | 說明 |
|--------|------|
| `frontend/` | Angular 問卷系統前端 |
| `backend/`  | Spring Boot 問卷後端 |
| `src/main/resources/schema.sql` | 資料表建立 SQL |
| `src/main/resources/data.sql`   | 問卷與填答假資料 |

---

## 📊 測試資料說明

啟動後端後，資料庫內會有：

- 問卷（quiz）共 4 份
- 題目（question）每份問卷 5 題
- 回覆紀錄（feedback）多筆，含不同使用者填寫資料

---

## 📌 注意事項

- 問卷統計圖表需搭配 `Chart.js` 正確顯示
- 本專案預設為 local 開發模式，請確認前後端連線設定無誤

---

## 🙌 聯絡我

如果你對本專案有興趣或建議，歡迎前往 GitHub 留言或聯絡我！
