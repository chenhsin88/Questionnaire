# Questionnaire 動態問卷系統

本專案為動態問卷系統，使用 Angular 17 製作前端、Spring Boot 開發後端，並搭配 MySQL 資料庫儲存問卷、題目與填答資料。  
本系統支援問卷建立、題型管理、使用者填寫與圖表化統計結果，適合應用於意見調查、學習測驗、行銷調研等場景。

---

## 功能特色

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

## 使用技術

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

## 快速開始（後端）

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

## 快速開始（前端）

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

## 專案結構
### 🔹 前端（[Frontend Repo](https://github.com/chenhsin88/Questionnaire)）

### 🔸 後端（[Backend Repo](https://github.com/chenhsin88/quiz14)）

---

## 注意事項
- 專案首頁 http://localhost:4200/list

- 問卷列表需搭配 Angular Material 正確顯示

- 問卷統計圖表需搭配 Chart.js 正確顯示

- 登入頁按登入即可進入後台管理者頁面

---

## 畫面示意

### 管理者-問卷列表頁
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/b798d6ce-f583-4e08-9643-ab54a2a67567" />

### 管理者-問卷題目編輯頁
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/4d8840a0-a88b-4cf6-97f6-98f97b876902" />

### 管理者-問卷名稱、說明、日期編輯頁
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/4381964d-7617-4350-a97e-ab47d96f6494" />

### 管理者-問卷填寫紀錄列表頁
<img width="400" height="450" alt="localhost_4200_result_feedback_1_id=1 (1)" src="https://github.com/user-attachments/assets/7334c54c-a891-4836-a022-f1c0ca5e238b" />

### 管理者-使用者填寫紀錄頁
<img width="400" height="450" alt="localhost_4200_result_feedback_1_id=1" src="https://github.com/user-attachments/assets/debba036-299a-4179-bad0-7736462ec8d0" />

### 管理者/使用者-統計頁
<img width="300" height="450" alt="localhost_4200_answer_id=2 (2)" src="https://github.com/user-attachments/assets/bfaf7483-1dcf-433a-a49c-61edf6cd6595" />

### 使用者-問卷填寫頁
<img width="300" height="450" alt="localhost_4200_answer_id=2 (1)" src="https://github.com/user-attachments/assets/eb76ce78-76d8-43d7-a48a-dd5964c64305" />





