# 終於講到 6.0 的改變了！聊 Laravel LazyCollection

開始用到 Laravel 的 Eloquent Model 和 Collection 了！趁這個機會，我們來聊聊 Laravel 6.0 的一個改進：LazyCollection

假設我們需要列出所有 User 的名稱，根據上次的教學，我們會想要

```php

$users = User::all();

```

這樣的程式在大多數的時候，都是不會有問題的


但是！

如果今天我們的網站越來越多人用，User 的個數不再只是幾個，而是幾百萬，幾千萬個，這會導致什麼問題呢？

~~這代表網站很賺錢，工程師應該要加薪了~~

我們之前取出的 `$users` 將會變得很大！

## PHP generator 和 yield

要理解 Laravel 做了什麼來解決這個問題，首先我們要學習一個 PHP 的新語法： yield

yield 這個語法是在 php 5.5 引進，


## LazyCollection

這裏不深究 Laravel 的 LazyCollection 是怎麼實作。我們只需要知道，利用這個新的語法，LazyCollection 取得的不再是一個陣列，而是一個 generator 物件

利用 `cursor()` 這個語法，我們可以不回傳一個 `Collection` 物件，而是收到一個 `LazyCollection` 物件

```php
$users = App\User::cursor();
```

既然取得的是 generator 而非一個陣列的包裝，那麼我們就可以知道，這樣的物件所消耗的記憶體，並不會如實際資料量那麼大。

我們可以很直觀的把 `$users` 這個物件當作 `Collection` 一樣使用，不用擔心記憶體過量：
```php

```
