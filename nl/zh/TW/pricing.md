---

copyright:
  years: 2016,2018
lastupdated: "2018-01-03"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# 定價
{: #pricing}

## 基本配置

{{site.data.keyword.composeForRedis_full}} 服務一開始有兩個 Redis/Sentinel 節點，每個節點有 256 MB 的記憶體及 256 MB 的儲存空間，這等於 1 個資源單位。服務_包括_ 抄寫及高可用性，因此每個單位及單價_包括_ 這兩個節點中資源的成本。

基本配置也包括專用的 Sentinel 節點（用來處理抄寫）及 HAProxy 入口網站（用來管理連線）。Sentinel 節點及 HAProxy 入口網站每個都有 64 MB 的記憶體。

基本服務配置具有固定價格。請參閱 {{site.data.keyword.cloud_notm}} 上的型錄磚，以取得當地貨幣的基本定價。例如，以美元計價的基本價為 $13/月。

## 增加資源

如果您的服務需要額外的記憶體，則可以使用磁碟儲存空間與記憶體單位比 1:1 的比例來增加配置的資源。{{site.data.keyword.composeForRedis}} 單位由 256 MB 的儲存空間與 256 MB 的記憶體所組成，而且每個單位及單價_包括_ 在這兩個節點上增加資源的成本。

## 計算部署的成本
{: #tiered-pricing}

每個額外單位（256 MB 儲存空間/256 MB 記憶體）都有單價，它會以當地貨幣列在服務的 {{site.data.keyword.cloud_notm}} 型錄磚上。以美元計價時，每個額外單位的成本為 $13。當您的所有 {{site.data.keyword.composeForRedis}} 服務的大小_總計_ 增加時，單價就會降低，如下面分級定價表所示。

單位數|單價
----------|-----------
1 - 9 個單位|基本單價 -- $13.00 美元/單位
10 - 24 個單位|折價 10% --$11.70 美元/單位
25 - 49 個單位|折價 20% -- $10.40 美元/單位
50 - 99 個單位|折價 30% -- $9.10 美元/單位
100 - 499 個單位|折價 40% --$7.80 美元/單位
500 - 999 個單位|折價 50% -- $6.50 美元/單位
1,000 - 4,999 個單位|折價 60% -- $5.20 美元/單位
5,000 個以上單位|折價 70% -- $3.90 美元/單位
{: caption="表 1. {{site.data.keyword.composeForRedis}} 分級定價" caption-side="top"}

