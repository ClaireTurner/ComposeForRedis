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

# 料金設定
{: #pricing}

## 基本構成

{{site.data.keyword.composeForRedis_full}} サービスの開始時には 2 つの redis/sentinel ノードがあり、それぞれのノードに 256MB のメモリーと 256MB のストレージ (1 ユニット分のリソースに相当) があります。 サービスには複製機能と高可用性機能が_含まれて_いるので、各ユニットとユニット単価には、両方のノードのリソースのコストが_含まれて_います。

基本構成には、複製を処理するための専用の sentinel ノードと、接続を管理するための HAProxy ポータルも含まれています。 sentinel ノードと HAProxy ポータルには、それぞれに 64MB のメモリーがあります。

基本サービス構成には、設定された価格があります。 現地通貨での基本料金設定については、{{site.data.keyword.cloud_notm}} のカタログ・タイルを参照してください。 例えば、米ドルでの基本価格は $13/月です。

## リソースを増やす

サービスのメモリーを追加する必要がある場合は、ディスク・ストレージ対メモリー・ユニットの割り振りリソースの比率が 1:1 になるような仕方で、割り振るリソースを増やすことができます。 {{site.data.keyword.composeForRedis}} の 1 ユニットは、256MB のストレージと 256MB のメモリーで構成されており、各ユニットとユニット単価には、両方のノードでリソースを増やすためのコストが_含まれて_います。

## デプロイメントのコストを計算する
{: #tiered-pricing}

追加のユニットについては、1 ユニット (256MB ストレージ/256MB メモリー) ごとの単価が設定されています。現地通貨でのこの価格は、サービスの {{site.data.keyword.cloud_notm}} カタログ・タイルで確認できます。 追加の 1 ユニットの米ドルでの価格は $13 です。 すべての {{site.data.keyword.composeForRedis}} サービスの_合計_サイズが増えると、ユニット単価が下がります。これについては、下記の段階的な価格設定の表をご覧ください。

ユニット数|ユニット単価
----------|-----------
1 - 9 ユニット|ユニットあたりの基本料金 -- $13.00 USD/ユニット
10 - 24 ユニット|10% 割引 --$11.70 USD/ユニット
25 - 49 ユニット|20% 割引 -- $10.40 USD/ユニット
50 - 99 ユニット|30% 割引 -- $9.10 USD/ユニット
100 - 499 ユニット|40% 割引 --$7.80 USD/ユニット
500 - 999 ユニット|50% 割引 -- $6.50 USD/ユニット
1,000 - 4,999 ユニット|60% 割引 -- $5.20 USD/ユニット
5,000 ユニット以上|70% 割引 -- $3.90 USD/ユニット
{: caption="表 1. {{site.data.keyword.composeForRedis}} の段階的な料金設定" caption-side="top"}

