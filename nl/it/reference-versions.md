---
copyright:
  years: 2016,2018
lastupdated: "2018-06-14"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# Versioni 
{: #facts-and-figures}

## Versioni (supportate e distribuite)

Versioni distribuibili| Versione preferita
----------|-----------
3.2.12, 4.0.10 | 4.0.10
{: caption="Tabella 1. Versioni Redis" caption-side="top"}

## Versione preferita

La versione preferita è di norma la versione più recente del database Redis disponibile per {{site.data.keyword.composeForRedis}}. È la versione che corrisponde al valore predefinito nel selettore della versione a discesa nella pagina del catalogo. È anche la versione di cui viene seguito automaticamente il provisioning dall'API se non viene specificata alcuna versione nella chiamata.

### Nuovo protocollo di versione preferito

Quando viene resa disponibile una nuova versione, il suo rilascio viene annunciato ed è disponibile per la distribuzione. Dopo la data di rilascio, c'è una finestra di circa 7 giorni in cui la versione più recente è disponibile ma non è la versione preferita. Questa finestra ti consente di distribuire e verificare la nuova versione, continuando però a disporre della versione corrente. Alla fine della finestra di 7 giorni, la nuova versione viene impostata come versione preferita oppure viene annunciata una nuova data per questa modifica.

L'elenco di versioni disponibili per il provisioning è disponibile nella {{site.data.keyword.composeForRedis}} [pagina di catalogo](https://console.{DomainName}/catalog/services/compose-for-redis).

Per ottenere un elenco corrente di versioni disponibili per il tuo servizio {{site.data.keyword.composeForRedis}} puoi utilizzare l'endpoint
[GET /2016-07/deployments/:id/versions](https://apidocs.compose.com/v1.0/reference#2016-07-get-deployments-versions).
