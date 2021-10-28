---
id: api-server
title: API Server
---
Api-Server is the core of the Leverege Platform. It interacts with all the micro-services and contains all of the rest routes that the Imagine UI interacts with.

Documentation for all of the routes available can be found at [Leverege Api](http://docs.leverege.com/imagine-api.html). The routes allow access to every aspect of the Leverege System. Routes can be used to create Blueprints, devices, users, projects and Systems. It can also be used to edit and view them. There are routes to interact with most of the micro-services. 

## Configuration

#### Required

| Name | Description |
| ---- | ----------- |
| MODEL_FIREBASE_SERVICE_ACCOUNT | service account key to firebase database for models |
| MODEL_FIREBASE_DATABASE_URL | url to firebase database for models |
| TEMPLATE_DIR | path to the directory templates are stored |
| LOCAL_AUTH_SECRET | local secret for connecting to the Auth server or service |
| AUTH0_DOMAIN | domain name for Auth0 authentication |
| AUTH0_CLIENT_ID | client id for Auth0 |
| AUTH0_CLIENT_SECRET | client secret for Auth0 |
| AUTH0_CLIENT_SECRET_B64 | Base 64 encoded key for Auth0 |
| DATA_FIREBASE_CONFIG | firebase database config |
| DATA_FIREBASE_SERVICE_ACCOUNT | firebase database service account |
| DATA_BIGQUERY_SERVICE_ACCOUNT | BigQuery database service account |
| DATA_BIGQUERY_PROJECT | BigQuery database project | 
| SQL_USER | sql user |
| SQL_PASSWORD | sql password |
| SQL_HOST | sql host |
| SQL_PORT | sql port |
| SQL_CA | sql ssl ca |
| SQL_CLIENT_CERT | sql ssl cert |
| SQL_CLIENT_KEY | sql ssl key |
| PG_USER | postgreSQL user | 
| PG_PASSWORD | postgreSQL password | 
| PG_DATABASE | postgreSQL database | 
| SIMULATOR_URL | url to where simulator is hosted |
| MODEL_SQL_USER | user of model sql db | 
| MODEL_SQL_PASSWORD | password of model sql db | 
| NPMRC_VALUE | contents will be made into .npmrc file | 

#### Optional

| Name | Description | Default | 
| ---- | ----------- | ------- |
| APP_NAME | name of app for firebase config | `'api-server'` |
| SQL_CA | sql ssl ca | `undefined` |
| SQL_CLIENT_CERT | sql ssl cert | `undefined` |
| SQL_CLIENT_KEY | sql ssl key | `undefined` |
| TRANSPORT_CONFIG | config for readers and writers | `{ type, host, port }` |
| NSQ_HOST_ADDR | host address for NSQ, if TRANSPORT_CONFIG is not specified | `'127.0.0.1'` |
| NSQ_HOST_PORT | port for NSQ, if TRANSPORT_CONFIG is not specified | `4150` |
| SERVER_PORT | server port that api will listen on | `8181` |
| LOCAL_AUTH_ISSUER | auth token issuer | `'https://imagine.leverege.com'` |
| LOCAL_AUTH_AUDIENCE | auth token audience | `''` |
| LOCAL_AUTH_EXPIRATION | expiration time of auth token | `'1d'` |
| INITIAL_USERS | default user accounts for imagine | `null` |
| CACHE_CONFIG | configuration for the cache db | `{ type, connection : { host, port } }` |
| LOCK_CONFIG | configuration for the lock db | `{ type, connection : { host, port } }` |
| BQ_HISTORY_TAGS | tags that are applied to the BigQuery database | `'[ 'long' ]'` |
| SQL_POOL_CONNECTION_LIMIT | limit of the number of sql connections | `10` |
| MYSQL_HISTORY_TAGS | tags that are applied to the MySql database | `'[ 'short' ]'` |
| PG_POOL_CONNECTION_LIMIT | limit of the number of postgreSQL connections | `10` |
| PG_PORT | postgreSQL port | `5432` |
| PG_HOST | postgreSQL host | `'localhost'` |
| PG_HISTORY_TAGS | tags that are applied to the PostgreSQL database | `'[ 'tdb' ]'` |
| MODEL_SQL_HOST | model sql db host | `'localhost'` |
| MODEL_SQL_PORT | model sql db port | `3306` |
| API_SERVICE_TOPIC | topic that is assigned to the apiWorker message processor | `'api-service-topic'` |
| GCF_FIREBASE_SERVICE_ACCOUNT | service account for google cloud functions | DATA_FIREBASE_SERVICE_ACCOUNT |
| SCRIPT_BUILD_DIR | directory where scripts will be deployed to | `'/tmp'` |
| REASONER_LIB_VERSION | deployed reasoner version | `'1.0.7'` |
| SCHEDULER_URL | url where scheduler is hosted | `'http://localhost:9937'` |
