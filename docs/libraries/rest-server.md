---
id: rest-server
title: Rest Server
---

The Rest Server is a service that provides a way for systems outside of the Leverege Platform to send and receive messages from the Leverege Platform.

Rest Server contains two routes. The first route is for triggering `inboundDataEventMsg` which receives a http request, transforms it into a message, and then sends it into the Leverege Platform. The second route is for acknowledging outbound messages. Sending a http request to this endpoint starts an `inboundAckMsg` in the Leverege Platform. 

Rest server also has a message processor for receiving outbound messages on the topic `rest-outbound`. These outbound messages get transformed into http requests. After receiving the outbound message, a http request can can be sent back to this service to acknowledge the event.

## Configuration

#### Required

| Name | Description |
| ---- | ----------- |
| SRV_FIREBASE_SERVICE_ACCOUNT | Service account key to firebase database for remote store |
| SRV_FIREBASE_DATABASE_URL | url to firebase database for remote store |
| MODEL_FIREBASE_SERVICE_ACCOUNT | service account key to firebase database for models |
| MODEL_FIREBASE_DATABASE_URL | url to firebase database for models |

#### Optional

| Name | Description | Default |
| ---- | ----------- | ------- |
| TRANSPORT_CONFIG | config for readers and writers | `{ type, host, port }` |
| NSQ_HOST_ADDR | host address for NSQ, if TRANSPORT_CONFIG is not specified | `'127.0.0.1'` |
| NSQ_HOST_PORT | port for NSQ, if TRANSPORT_CONFIG is not specified | `4150` |
| REST_SERVER_PORT | server port that the server listens on | `8183` |
