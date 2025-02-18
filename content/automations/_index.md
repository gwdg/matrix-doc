---
title: "Automatisierungen"
date: 2025-02-17T19:11:00+02:00
chapter: false
draft: false
---

## Automatisierungen und Bots

Möchte man sich in Matrix automatisiert Nachrichten in einem Raum erzeugen lassen, funktioniert die API auf Grund der SSO-Authentifizierung nicht direkt, stattdessen kann hierfür die Academiccloud Bot-Instanz genutzt werden.

Die Möglichkeiten sind hier sehr vielfältig, Anwendungsbeispiele könnten sein:

- Automatisierte Willkommensnachrichten für neue Raum-Mitglieder
- Erstellen von Toots in Mastodon
- Automatisches Erinnern an Termineinladungen
- Automatisches Benachrichtigen bei Änderungen an Software-Repositories
- Automatische Nachrichten bei Störungen an Web-Diensten
- ...

Je nach Anwendungsfall kann hierzu ein sog. _Hookshot_ Nutzer genutzt werden, welcher nur in einem Raum mit entsprechenden Berechtigungen hinzugefügt werden muss und daraufhin in wenigen Schritten für RSS Feeds, Gitlab Events oder Webhooks genutzt werden kann.

Möchte man allgemeiner auch auf bestimmte Events in einem Raum - z.B. das Beitreten einer Nutzerin - reagieren, so kann hierfür ein Bot-Account erzeugt werden, mit dessen Hilfe können dann beliebige Nachrichten über die Client-Server API erzeugt werden, diese werden dann im Namen des Bot-Accounts erzeugt.


## Hookshot-User {#hookshot-user}

Um den Hookshot zu nutzen, muss der Hookshot-User `@hookshot:gwdg.de` von der GWDG-Instanz in einem Raum eingeladen und das Power-Level 'Moderator' gegeben werden. Daraufhin kann mit der Chatnachricht

```
!hookshot feed <url>
bzw.
!hookshot webhook <kreativerName>
```

ein RSS-Feed abonniert bzw. ein neuer Webhook angelegt werden. Im Falle des Webhook werden die nötigen Infos (Token/ URL) als persönliche Nachricht durch den Hookshot-User verschickt.

Eine Nachricht kann nun z.B. so erstellt werden:
```
curl -X PUT https://hook.matrix.gwdg.de/webhook/ffffff-fffff-ffff-ffff-ffffffffffff -H "Content-Type: application/json" -d '{"text": "The answer is 42."}'
```

Alle möglichen Befehle listet
```
!hookshot help
```
auf. Weitere Informationen [auf der Website des hookshot-Bots](https://matrix-org.github.io/matrix-hookshot/latest/setup/webhooks.html).

## Bot-User {#bot-user}

Für maximale Flexibilität können Bot-Accounts genutzt werden, diese existieren auf einer eigenen Matrix Instanz, d.h. Bots haben als Home-Server immer `bot.academiccloud.de`. Die Schritte, um einen Bot-Account zu erhalten, sind:

1. Auf idm.gwdg.de den User-Knopf oben rechts klicken und die Seite der "Anwendungsspezifischen Zugangsdaten" öffnen.
2. Im linken Reiter den Punkt "Matrix: Zugangsdaten für Bots" auswählen, die nötigen Daten ausfüllen und "Zugangsdaten generieren" klicken.
3. Es wird ein Benutzername und ein Token erzeugt. Der Benutzername stellt auch gleichzeitig den Namen des Bots dar, z.B. Benutzername `uXXXXX` übersetzt sich später zu `uXXXXX:bot.academiccloud.de`. Der Token stellt das Passwort dar.
4. Es können nun Befehle der [Client-Server API](/clients/client-server-api) von Matrix genutzt werden - für ganz spezielle Sonderfälle müsste man im Zweifel noch prüfen, ob Synapse diese implementiert.

Auf der Seite [Cient-Server API](/clients/client-server-api) werden Minimalbeispiele gezeigt, wie per Bot-Account Befehle erzeugt werden können und auf bestehende Clients hingewiesen.

Möchte man nicht direkt die Client-Server API nutzen, gibt es auch Tools, die das etwas vereinfachen. Siehe hierzu z.B.:

- Hemppa: https://github.com/vranki/hemppa
- Maubot: https://github.com/maubot/maubot
- Opsdroid: https://opsdroid.dev
