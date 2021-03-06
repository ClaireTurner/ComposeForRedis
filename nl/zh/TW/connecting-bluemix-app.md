---

copyright:
  years: 2016,2018
lastupdated: "2018-05-09"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 連接 {{site.data.keyword.cloud_notm}} 應用程式

若要將 {{site.data.keyword.cloud}} 應用程式連接至您的服務，請使用佈建服務時所建立的服務認證。範例應用程式會示範如何使用 Node.js 利用所提供的認證連接至 {{site.data.keyword.composeForRedis_full}} 服務，以及如何建立資料庫、從資料庫讀取，和寫入資料庫。

## 使用 'Hello World' 範例應用程式來連接

[compose-redis-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-redis-helloworld-nodejs) 範例應用程式會示範如何使用 Node.js 利用所提供的認證連接至 {{site.data.keyword.composeForRedis}} 服務。應用程式會建立、讀取及寫入資料庫。

請下載範例應用程式，並遵循 Readme 檔中的指示。然後，在 {{site.data.keyword.cloud_notm}} 的應用程式詳細資料頁面中，按一下**檢視應用程式**來檢視*範例* 表格的內容。

## 可用的認證

欄位名稱|說明
----------|-----------
`uri`|要在連接至服務時使用的 URI，包括綱目 (redis:)、管理使用者名稱和密碼、伺服器的主機名稱，以及要連接至的埠號。
`uri_direct_1`|可以在連接至服務時使用的第二 URI。格式與 `uri` 相同。
`ca_certificate_base64``（選用）`|用來確認應用程式將連接至適當伺服器的 base64 編碼自簽憑證。憑證只存在於具有自簽憑證而非 Let's Encrypt 憑證的服務上。您需要先將金鑰解碼，才能使用金鑰（如範例應用程式中所示）。
`uri_cli`|連接至資料庫實例的 `redis-cli` 指令行。
`deployment_id`|Compose 內所建立之服務的內部 ID。
`db_type`|服務所提供的資料庫類型；在此情況下，為 `redis`。
`name`|資料庫部署名稱。
{: caption="表 1. Compose for Redis 認證" caption-side="top"}

**附註：**兩個 `haproxy` 入口網站都可以存取 Redis 服務。`uri` 及 `uri_direct_1` 都可以用來連接。在應用程式中，切換 `uri` 與 `uri_direct_1`，以管理連線失敗的回應。
