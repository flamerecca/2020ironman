# [Day 3]框架裝好了那畫面呢？聊聊 docker 和 laradock

框架安裝好，檔案也都處理完了，資料夾結構的觀念也釐清了一部分。可是！都到第三天的教學了，現在還沒有看到畫面，怎麼回事？

對熟悉網頁開發的讀者來講，應該很清楚問題的癥結：雖然，目前網站上還沒有實際運行。

筆者這裡建議使用 docker 建構你的環境，這樣可以保證有一天，要是你希望網站對外公開時，能最大的減少環境所產生的風險。

* [Mac 用戶請看這個教學](https://docs.docker.com/docker-for-mac/install/)
* [Windows 用戶請看這個教學](https://docs.docker.com/docker-for-windows/install/)

>安裝時會要求你申請 docker Hub 網站的帳號 這不是什麼奇怪的網站，不用擔心，可以放心的申請。 

安裝好之後，我們在指令列確認一下是否安裝成功

然後，我們下載 laradock。在 `Laravel60demo/` 裡面，我們執行

```
$ git clone https://github.com/Laradock/laradock.git
```

下載到指定位置之後 我們嘗試

注意這邊的參數不能省略 省略了會一次用全部的 image 打開 docker container 
