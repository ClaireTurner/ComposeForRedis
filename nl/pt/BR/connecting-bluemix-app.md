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

# Conectando um aplicativo {{site.data.keyword.cloud_notm}}

Para conectar um aplicativo {{site.data.keyword.cloud}} a seu serviço, use as credenciais de serviço que são criadas quando o serviço é provisionado. O app de amostra demonstra como usar Node.js para se conectar a um serviço {{site.data.keyword.composeForRedis_full}} usando as credenciais fornecidas e como criar um banco de dados e ler e gravar no banco de dados.

## Conectando usando o aplicativo de amostra 'Hello World'

O aplicativo de amostra [compose-redis-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-redis-helloworld-nodejs) demonstra como usar o Node.js para se conectar a um serviço {{site.data.keyword.composeForRedis}} usando as credenciais fornecidas. O aplicativo cria, lê e grava em um banco de dados

Faça download do aplicativo de amostra e siga as instruções no arquivo leia-me. Em seguida, em sua página de detalhes do aplicativo no {{site.data.keyword.cloud_notm}}, clique em **Visualizar app** para visualizar os conteúdos da tabela *exemplos*.

## Credenciais disponíveis

Campo de nome|Descrição
----------|-----------
`uri`|O URI a ser usado na conexão com o serviço, que inclui o esquema (redis:), o nome do usuário administrativo e a senha, o nome do host do servidor e o número da porta à qual se conectar.
`uri_direct_1`|Um URI secundário que pode ser usado ao se conectar ao serviço. O formato é o mesmo que para `uri`.
` ca_certificate_base64 `  ` (opcional) `|Um certificado autoassinado codificado em base64 usado para confirmar se um aplicativo está se conectando ao servidor apropriado. O certificado está presente apenas em serviços que possuem um certificado autoassinado em vez de um certificado Let's Encrypt. É necessário decodificar a chave antes de poder usá-la, conforme mostrado no aplicativo de amostra.
`uri_cli`|Uma linha de comando `redis-cli` que se conecta à instância de banco de dados.
`deployment_id`|Um identificador interno para o serviço conforme criado no Compose.
`db_type`|O tipo de banco de dados que é oferecido pelo serviço; nesse caso, `redis`.
`name`|O nome da implementação do banco de dados.
{: caption="Tabela 1. Credenciais do Compose for Redis" caption-side="top"}

**Nota:** dois portais `haproxy` fornecem acesso ao serviço Redis. Tanto `uri` quanto `uri_direct_1` podem ser usados para a conexão. Em seus aplicativos, alterne entre `uri` e `uri_direct_1` para gerenciar respostas às falhas de conexão.
