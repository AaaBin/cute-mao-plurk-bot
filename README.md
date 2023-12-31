# README

> Tags: `GCP` `Cloud Run` `Plurk`

從[這篇製作教學](https://hackmd.io/xrJvVxtDQmy-Feu7mnVofQ)修改而來的噗浪機器人，只會回一個表符。

原本的範例中使用的是可以在有新噗時獲取即時的 **Comet channel API，但**換成 Polling 的方式，搭配 GCP 的 Cloud Run Job 以固定間隔執行。

調整內容（簡述）： 

- 改用 `os.environ.get` 的方式從環境變數中取得 API_KEY 等參數
- 改用 `/APP/Polling/getPlurks` 輪詢，搭配執行間隔的參數來撈取上次執行結束後的新噗，而不用全部撈取
- build 成 image 後由 Cloud Run Job 來執行，不需要程式隨時維持運行

## Reference

[python plurk api 2.0 噗浪機器人製作教學 - HackMD](https://hackmd.io/xrJvVxtDQmy-Feu7mnVofQ)

[噗浪機器人範例程式 – 使用 Plurk API 2.0](https://dada.tw/blog/2011/10/28/426/)

[Plurk API 2.0](https://www.plurk.com/API)

https://github.com/clsung/plurk-oauth
