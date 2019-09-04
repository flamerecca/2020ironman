# Hello World! 開啟我們自己的第一個網頁！

檔案安裝好了，環境也建置好了，再來就是要開始寫程式囉！

作為慣例，我們當然是來寫一個簡單的 Hello World，跟全世界介紹一下我們的網站吧！

## 設置路徑

首先，我們先想好我們 hello world 的網頁位址是什麼

既然是 hello world，那我們就用 `/hello-world` 這個路徑好了！

[http://127.0.0.1/hello-world](http://127.0.0.1/hello-world)

點進去之後，我們看到了

![404 畫面](https://i.imgur.com/SWNlzf2.png)

不意外的是 404 畫面，畢竟我們什麼都還沒開始寫嘛ＸＤ

----

在 Laravel 裡面，設置路徑的方式是在 `routes/` 資料夾裡面

我們打開這個資料夾，看看裡面的檔案結構

![Laravel Routes Structure](https://i.imgur.com/2oWXqhX.png)

>因為筆者自己喜歡的 IDE 是 PhpStorm，後面的教學畫面也通常會是以 PhpStorm 的畫面為主。
>
>非常建議讀者們如果經濟許可，可以買來在開發中使用，會節省非常多的開發時間！

打開 `web.php`，我們可以看到以下內容

```php
<?php

/*
|--------------------------------------------------------------------------
| Web Routes
|--------------------------------------------------------------------------
|
| Here is where you can register web routes for your application. These
| routes are loaded by the RouteServiceProvider within a group which
| contains the "web" middleware group. Now create something great!
|
*/

Route::get('/', function () {
    return view('welcome');
});
```

我們在檔案後面，加上

```php
Route::get('/hello-world');
```

然後連線看看～

>對不太熟悉 PHP 的讀者來說，可能感覺少了什麼步驟的感覺。
>
>沒錯！因為 PHP 是所謂的「直譯式語言」，這種程式語言只要改動程式碼，就可以馬上看到變更後的結果，不需要其他流程！

好的！我們再來看看剛剛的網址：

![Laravel 錯誤畫面](https://i.imgur.com/IjcbmRM.png)

欸⋯⋯雖然確實有畫面，但是好像跟我們預期的不太一樣耶！

## hello world!



不要懷疑！就是這麼的簡單，我們現在連線到
 
就可以看到我們的 `hello world!` 了！

## 設計畫面

雖然看到文字很棒，但是只有純文字的畫面，怎麼能讓我們滿意呢？

所以！我們要設計畫面了！

首先我們建立 `resources/views/hello_world.blade.php`

```php
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Hello World!</title>
    </head>
    <body>
      Hello World!
    </body>
</html>
```
