# 建立資料庫！Laravel 怎麼做資料庫遷移和預設資料

處理完

但是，首先我們要來聊另一個網站很重要的部分：資料庫

## 資料庫遷移（Database Migration）

如果你是用傳統的 Relational database，資料庫架構的維護常常是一個難題。

怎麼保證所有人的開發環境，資料庫結構都是一致的，又怎麼紀錄並讓所有開發者同步資料庫的改動，常常是許多人感到頭痛的問題。

幸好！

資料庫遷徙（migration）的概念，就是用程式碼來改動資料庫的結構。由於程式碼是在版本控制裡面的

（如果某個開發者版本控制就出錯⋯⋯那基本上他拿到的程式碼也不見得正確，本來就無法正常開發了。

對他來說更重要的事情應該不是資料庫結構，而是趕快更新他的程式碼版本）

## 資料庫植入（Database Seeding）
