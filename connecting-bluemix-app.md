---

copyright:
  years: 2016,2017
lastupdated: "2017-06-16"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Connecting a Bluemix application

To connect a Bluemix application to your service, use the service credentials that are created when the service is provisioned. The sample app demonstrates how to use Node.js to connect to a {{site.data.keyword.composeForRedis}} service using the provided credentials, and how to create a database and read from and write to the database.

## Connecting using the 'Hello World' sample app

The [compose-redis-helloworld-nodejs](https://github.com/IBM-Bluemix/compose-redis-helloworld-nodejs) sample app demonstrates how to use Node.js to connect to a {{site.data.keyword.composeForRedis}} service using the provided credentials. The application creates, reads from, and writes to a database

Download the sample app and follow the instructions in the readme file. Then, in your application details page in Bluemix, click **View APP** to view the contents of the *examples* table.

## Available credentials

Field Name|Description
----------|-----------
`uri`|The URI to be used when connecting to the service, which includes the schema (redis:), admin user name and password, the host name of the server and the port number to connect to.
`uri_cli`|A `redis-cli` command line that connects to the database instance.
`deployment_id`|An internal identifier for the service as created within Compose.
`db_type`|The type of database that is offered by the service; in this case `redis`.
`name`|The database deployment name.
{: caption="Table 1. Compose for Redis credentials" caption-side="top"}
