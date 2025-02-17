---
title: "Client-Server API"
date: 2025-02-17T19:51:00+02:00
chapter: false
draft: false
---

## Client-Server API

Mithilfe der [Client-Server API](https://spec.matrix.org/latest/client-server-api/) kann programmatisch mit einem Matrix Homeserver kommuniziert werden. Mit der API kann sich ein Client authentifizieren, Raum-Events abrufen und erzeugen und mehr. Im Folgenden wird vorausgesetzt, dass ein [Bot-User](/automations/_index.md) existiert.

Bevor komplette Clients nachprogrammiert werden, lohnt es sich zunächst [existierende Clients](#existing-clients) zu prüfen.

### Authentifizierung {#example-auth}

Zunächst muss der Bot-Account `uXXXXX` sich an der Bot-Instanz authentifizieren, wodurch ein temporär gültiger Zugangstoken erzeugt wird.

```sh
curl -X POST "https://bot.academiccloud.de/_matrix/client/v3/login" -d \
	'{
	"type": "m.login.password",
	"user": "uXXXXX",
	"password": "<Passwort bzw. Token aus dem IDM>"
	}'
```

Bei Erfolg sieht eine Antwort in etwa wie folgt aus:
```
{"user_id":"@uXXXXX:bot.academiccloud.de","access_token":"<ACCESS_TOKEN>","home_server":"bot.academiccloud.de","device_id":"<DEVICE_ID>","well_known":{"m.homeserver":{"base_url":"https://bot.academiccloud.de/"}}}
```

Der `<ACCESS_TOKEN>` ist im Folgenden der zu nutzende Token.


### Sende Nachricht in einen Raum {#example-write}

Mit diesem Befehl kann eine simple Text-Nachricht in einen Raum gesendet werden:

```sh
curl -X PUT "https://bot.academiccloud.de/_matrix/client/v3/rooms/%21<RAUM_ID>:<HOME_SERVER>/send/m.room.message/$(uuidgen)" \
     -H "Authorization: Bearer <ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -d '{
           "msgtype": "m.text",
           "body": "Hello, world!"
         }'
```

### Höre auf Nachricht in Räumen {#example-listen}

Ebenso lässt sich auch auf Nachrichten hören (Achtung: Nachrichten aus allen Räumen, in denen der Bot Mitglied ist):

```sh
curl -X GET "https://bot.academiccloud.de/_matrix/client/v3/sync?timeout=3600" \
	-H "Authorization: Bearer <ACCESS_TOKEN>"
```

Das lässt sich über Filter weiter einschränken.

## Existierende Clients {#existing-clients}
Als Referenz ein paar Beispiele für bestehende Clients / SDKs:

- Mautrix-Go (Go): https://github.com/mautrix/go
- Matrix-Nio (Python): https://github.com/matrix-nio/matrix-nio
- Matrix-Bot-SDK (Javascript): https://github.com/turt2live/matrix-bot-sdk

Etwas fortgeschrittenere Clients:

- Hemppa: https://github.com/vranki/hemppa
- Maubot: https://github.com/maubot/maubot
- Opsdroid: https://opsdroid.dev
