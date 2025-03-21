# Laravel 12 使其符合歐洲一般資料保護規定 Cookie 法規

引入 scify 的 laravel-cookie-guard 套件來擴增使其符合歐洲一般資料保護規定 Cookie 法規，其適用對象為在歐洲地區設立據點或為歐洲使用者提供服務的企業和機構，Cookie 同意政策視窗是歐洲國家為保護消費者隱私而引入的重要措施，確保用戶了解 Cookie 的使用方式並能夠自主決定。Cookie 在網站上扮演著重要的角色，提供個性化體驗和方便的功能。然而，如果使用者拒絕使用 Cookie，一些網站可能無法提供某些功能，並且用戶可能會失去個性化的使用體驗。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __migrate__ 來執行所有未完成的遷移。
```sh
$ php artisan migrate
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/` 來進入歡迎頁面。

----

## 畫面截圖
![](https://i.imgur.com/ldIVsHz.png)
> 必須獲得用戶明確的授權和知情同意，才能在他們的設備上存儲和訪問 Cookie

![](https://i.imgur.com/HfSAy7Y.png)
> 讓用戶瞭解網站如何使用他們的數據，以及他們的數據將用於什麼目的
