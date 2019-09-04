# [Day 3]框架裝好了，那畫面呢？聊聊 docker 和 laradock

框架安裝好，檔案也都處理完了，資料夾結構的觀念也釐清了一部分。可是！都到第三天的教學了，現在還沒有看到畫面，怎麼回事？

對熟悉網頁開發的讀者來講，應該很清楚問題的癥結：雖然，目前網站上還沒有實際運行。

筆者這裡，建議使用 docker 建構你的測試環境，這樣可以保證有一天，要是你希望網站對外公開時，能最大的減少環境所產生的風險。雖然學習 docker 需要不少時間成本，但是相當值得！

首先，是在你的開發機器上面安裝 docker：

* [Mac 用戶請看這個教學](https://docs.docker.com/docker-for-mac/install/)
* [Windows 用戶請看這個教學](https://docs.docker.com/docker-for-windows/install/)

>安裝時會要求你申請 docker Hub 網站的帳號 這不是什麼奇怪的網站，不用擔心，可以放心的申請。 

依照步驟安裝好之後，我們在指令列裡面，確認一下是否安裝成功

```shell
$ docker --version

Docker version 19.03.1, build 74b1e89
```

如果能成功地看到安裝的 docker 版本訊息，那麼恭喜你！你已經安裝成功了

接著



----

什麼是 Laradock 呢？

![laradock logo](https://raw.githubusercontent.com/laradock/laradock/master/.github/home-page-images/laradock-logo.jpg)



然後，我們下載 Laradock。在 `Laravel60demo/` 裡面，我們執行

```
$ git clone https://github.com/Laradock/laradock.git
```

下載到指定位置之後，我們進入到 `laradock/` 資料夾看看內容。

```shell
$ cd laradock
$ ls

```
確認下載完成了，檔案也沒有問題，我們準備運行

運行 Laradock 之前，我們記得建立好 Laradock 所需的 `.env` 檔案，這邊我們先使用原本就附加的範例檔案 `env-example`。

在 `laradock/` 資料夾裡面執行

```
$ cp env-example .env
```

確認建立好 `.env` 之後，我們來開啟運行網站所需的服務

```
$ docker-compose up -d nginx mysql workspace 
```
>注意這邊的參數不能省略！省略了會一次打開所有的服務，電腦很快就撐不住了 ！
>
>跟官網的範例不一樣，筆者這邊移除了部分的服務，這樣讓之後的教學更加單純。


