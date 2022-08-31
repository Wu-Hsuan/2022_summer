# 當季食材小幫手—食材問題諮詢機器人
- discord


###### tags: `Droidtown`

Bot 可以回覆的問題
-------------
* 推薦當季食材 
* 如何挑選特定食材 
* 特定食材的價格 
* 推薦與食材相關料理
* 食材相關的食用禁忌 

DEMO
-------------
{%youtube [Demo](https://www.youtube.com/watch?v=-nN0iRo6ejM) %}

檔案總覽/目錄
-------------
```
.
├── ingredient_bot.py  # main program，執行以啟動 bot，處理與 discord 間的互動
├── Loki.py            # 主要使用到 function runLoki 
├── model.py           # NLU model 以及相關的 function
├── README.md
├── requirements.txt
│  
├─ info 
│  ├── ingredient.json # 紀錄每個月份的當季食材
│  └── inSeason.json   # 紀錄每個食材的作法、挑法與禁忌
│      
├─ intent # 所有的 intent 都放在這邊
│  ├── Loki_all_ingre.py
│  ├── Loki_capability.py
│  ├── Loki_CheckInSeason.py
│  ├── Loki_InSeason.py
│  ├── Loki_price.py
│  ├── Loki_recipe.py
│  ├── Loki_recommend.py
│  ├── Loki_reject.py
│  ├── Loki_selection.py
│  ├── Loki_taboo.py
│  ├── Loki_which_season.py
│  ├── Updater.py
│  └── USER_DEFINED.json
│          
└─ ref # 啟用 Loki 服務時，需要將裡面的所有檔案匯入 Loki project 中
   ├── all_ingre.ref
   ├── capability.ref
   ├── CheckInSeason.ref
   ├── InSeason.ref
   ├── price.ref
   ├── recipe.ref
   ├── recommend.ref
   ├── reject.ref
   ├── selection.ref
   ├── taboo.ref
   └── which_season.ref
```

設置環境
-------------
- 環境需求
    - Python 3 or above
    - pip or pip3 is installed
- 安裝相關套件
    - 執行指令：`$ pip install -r requirements.txt`

建立 Discord Bot
-------------
1. 進入 [Discord Developer](https://discord.com/developers/applications) 後登入Discord帳號
2. 點擊右上角的New Application，在Name的欄位中輸入機器人名稱
3. 新增一個Bot，在BOT PERMISSIONS的欄位勾選Sends Messages、Embed Links、Attach Files及Read Message History
4. 將Bot加入伺服器
5. 將複製下來的 token 貼上到檔案 account.info 中： <-這個要加在哪個步驟(我覺得要要不放在上面備註，要不讓使用者自己決定要不要用這個，因為其實可以直接輸在程式裡)
```
{
    "username" : "",
    "apikey_ing" : "",
    "discord_token": " ***將 token 貼到這裡*** "
}
```

啟用 Loki 服務
-------------
1. 登入後進入 [Loki 控制台](https://api.droidtown.co/loki/)
2. 輸入專案名稱，點選 `建立專案`
3. 點選剛建立完成的專案名稱以進入專案
4. 點選 `選擇檔案` > 選擇所有 ref 內的檔案 > 點選 `讀取意圖`
5. 點選左上角房子圖示，回到 [Loki 控制台](https://api.droidtown.co/loki/)，點選 `複製` 專案金鑰
6. 將複製下來的金鑰貼上到檔案 account.info 中：
```
{
    "username" : " ***輸入USERNAME(註冊信箱)*** ",
    "apikey_ing" : " ***將專案金鑰貼到這裡*** ",
    "discord_token": ""
}
```

執行以啟動 Ingredient Bot / 當季食材小幫手
-------------
- 執行指令：`$ python ingredient_bot.py`

引用資料
-------------
* [icook](https://icook.tw/)
* [Cookpad](https://cookpad.com/tw)
* [台北農產運銷股份有限公司](http://www.tapmc.com.taipei/)
* [農業知識入口網](https://kmweb.coa.gov.tw/)
* [美食天下](https://www.meishichina.com/)

參考文件
-------------
[卓騰語言科技產品說明文件](https://api.droidtown.co/document/)

聯絡資訊
-------------
若您還有其他任何的疑問，或是對 Loki 與食材相關的問題有興趣 

歡迎透過E-mail聯繫，謝謝 

Joe Huang：[joehuangx@gmail.com](mailto:joehuangx@gmail.com)      

Lisi Yang：[lisi16810@gmail.com](mailto:lisi16810@gmail.com)







