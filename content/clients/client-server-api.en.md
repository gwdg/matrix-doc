---
title: "Client-Server API"
date: 2025-02-17T19:51:00+02:00
chapter: false
draft: false
---

## Client-Server API

The [Client-Server API](https://spec.matrix.org/latest/client-server-api) allows programmatic communication with a Matrix homeserver. Using this API, a client can authenticate, retrieve and send room events, and perform other
operations. The following examples assume that a [bot user](/automations#bot-user) already exists.

Before implementing a complete client from scratch, it is recommended to check [existing clients](#existing-clients) first.

### Authentication {#example-auth}
Firstly, the bot account `uXXXXX` needs to authenticate with the bot instance. This process generates a temporary access token.

```
curl -X POST "https://bot.academiccloud.de/_matrix/client/v3/login" -d \
    '{
    "type": "m.login.password",
    "user": "uXXXXX",
    "password": "<Password or token from IDM>"
    }'
``` 

If successful, the response will look something like this:

``` 
{"user_id":"@uXXXXX:bot.academiccloud.de","access_token":"<ACCESS_TOKEN>","home_server":"bot.academiccloud.de","device_id":"<DEVICE_ID>","well_known":{"m.homeserver":{"base_url":"https://bot.academiccloud.de/"}}}
``` 

The `<ACCESS_TOKEN>` from this response must be used in subsequent API requests.

### Send a Message to a Room {#example-write}
The following command sends a simple text message to a room:

```
curl -X PUT "https://bot.academiccloud.de/_matrix/client/v3/rooms/%21<ROOM_ID>:<HOME_SERVER>/send/m.room.message/$(uuidgen)" \
     -H "Authorization: Bearer <ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -d '{
           "msgtype": "m.text",
           "body": "Hello, world!"
         }'
```

### Listen for Messages in Rooms {#example-listen}
You can listen for incoming messages in all rooms where the bot is a member using:

```
curl -X GET "https://bot.academiccloud.de/_matrix/client/v3/sync?timeout=3600" \
    -H "Authorization: Bearer <ACCESS_TOKEN>"
```

To limit this to specific rooms or event types, filters can be applied.

## Existing Clients {#existing-clients}

Here are some examples of existing Matrix clients and SDKs for reference:

- Mautrix-Go (Go): https://github.com/mautrix/go
- Matrix-Nio (Python): https://github.com/poljar/matrix-nio
- Matrix-Bot-SDK (JavaScript): https://github.com/turt2live/matrix-bot-sdk
