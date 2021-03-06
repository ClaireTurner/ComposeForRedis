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

# 连接 {{site.data.keyword.cloud_notm}} 应用程序

要将 {{site.data.keyword.cloud}} 应用程序连接到服务，请使用供应服务时所创建的服务凭证。样本应用程序演示如何使用 Node.js，通过提供的凭证连接到 {{site.data.keyword.composeForRedis_full}} 服务，如何创建数据库以及如何对数据库进行读取和写入操作。

## 使用“Hello World”样本应用程序进行连接

[compose-redis-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-redis-helloworld-nodejs) 样本应用程序演示如何使用 Node.js，通过提供的凭证连接到 {{site.data.keyword.composeForRedis}} 服务。应用程序创建、读取和写入数据库

下载样本应用程序，并遵循自述文件中的指示信息。然后，在 {{site.data.keyword.cloud_notm}} 中的应用程序详细信息页面中，单击**查看应用程序**，以查看*示例*表的内容。

## 可用凭证

字段名称|描述
----------|-----------
`uri`|连接到服务时要使用的 URI，包括 (redis:)、管理用户名和密码、服务器的主机名和要连接到的端口号。
`uri_direct_1`|连接到服务时可使用的第二个 URI。格式与 `uri` 的相同。
`ca_certificate_base64``（可选）`|Base64 编码的自签名证书，用于确认应用程序连接到的是相应的服务器。在具有 Let's Encrypt 证书的服务上不提供该自签名证书。您需要先将密钥解码，才能加以使用，如样本应用程序中所示。
`uri_cli`|连接到数据库实例的 `redis-cli` 命令行。
`deployment_id`|在 Compose 内创建的服务的内部标识。
`db_type`|服务所提供的数据库类型；在本例中为 `redis`。
`name`|数据库部署名称。
{: caption="表 1. Compose for Redis 凭证" caption-side="top"}

**注：**两个 `haproxy` 门户网站提供对 Redis 服务的访问权。`uri` 和 `uri_direct_1` 都可用于连接。在您的应用程序中，在 `uri` 和 `uri_direct_1` 之间进行切换，以管理对连接失败的响应。
