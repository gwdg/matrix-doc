---
title: "Automatisierungen"
date: 2025-02-17T19:11:00+02:00
chapter: false
draft: false
---

## Automations and Bots
If you want to automatically generate messages in a Matrix room, the API does not work directly due to SSO authentication. Instead, you can use the Academiccloud Bot instance for this purpose.

There are many possible use cases, such as:

- Automated welcome messages for new room members
- Creating toots on Mastodon
- Automatic reminders for scheduled events
- Notifications for changes in software repositories
- Automatic alerts for disruptions in web services
- ...

Depending on the use case, a Hookshot user can be added to a room with the necessary permissions. This user can then be used in a few simple steps for RSS feeds, GitLab events, or webhooks.

If you need a more general solution to respond to certain room events (e.g., a user joining), a bot account can be created. This bot can send messages via the Client-Server API, and messages will appear in the room as coming from the bot.

## Hookshot-User {#hookshot-user}
To use hookshot, you must invite the hookshot user `@hookshot:gwdg.de` from the main instance into a room and grant it power level 'Moderator'. After that, you can subscribe to an RSS feed or create a new webhook with the following chat messages:

```
!hookshot feed <url>
bzw.
!hookshot webhook <kreativerName>
```

When creating a webhook, the necessary details (token/URL) will be sent via direct message from the Hookshot user.

To send a message via the webhook, you can use:
```
curl -X PUT https://hook.matrix.gwdg.de/webhook/ffffff-fffff-ffff-ffff-ffffffffffff -H "Content-Type: application/json" -d '{"text": "The answer is 42."}'
```

To see all available commands, use:

```
!hookshot help
```

For more details, check the [Hookshot bot documentation](https://matrix-org.github.io/matrix-hookshot/latest/setup/webhooks.html).

## Bot-User {#bot-user}
For maximum flexibility, bot accounts can be used. These accounts exist on a separate Matrix instance, meaning their home server is always `bot.academiccloud.de`. The steps for creating a bot-account are:

1. Go to idm.gwdg.de, click the User button in the top right corner, and open the "Application-Specific Access Credentials" page.
2. In the left menu, select "Matrix: Access Credentials for Bots", fill in the required details, and click "Generate Credentials".
3. A username and an access token will be generated. The username will also serve as the bot's identifier, e.g. username `uXXXXX` later translates to `uXXXXX:bot.academiccloud.de`. The token represents the password.
4. The bot can now interact with the [Client-Server API](/clients/client-server-api), for special cases it may be necessary to check whether synapse implements them.

On the [Client-Server API](/clients/client-server-api) page, you can find minimal code examples and references to useful clients.

If you do not want to directly use the Client-Server API, there are also some tools that simplify this. You may consider one of the following:

- Hemppa: https://github.com/vranki/hemppa
- Maubot: https://github.com/maubot/maubot
- Opsdroid: https://opsdroid.dev
