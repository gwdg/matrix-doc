---
title: "Migration"
date: 2024-09-26T13:45:15+02:00
draft: false
chapter: false
weight: 70
---
 
## End of chat.gwdg.de

Rocket.Chat will remain available after September 2024, but the licence will expire shortly before the end of September. From that point on, the following restrictions will apply:

- Mobile clients will no longer receive push notifications
- the online status of accounts (present/absent/busy/offline) will no longer be visible

It has not yet been decided when Rocket.Chat will finally be available and this will also depend on its use beyond the date of replacement. The aim is to give each user enough time to make the switch and to be able to change workflows. The switch is recommended for all users.

## Migrating to Matrix

With [migrate.chat.gwdg.de](https://migrate.chat.gwdg.de), a website is provided that allows you to move channels to Matrix if you have the ‘owner’ role. The entire history, including files, is copied, the original channel is set to read-only and a final message is posted in the channel. This channel is migrated to Matrix for **all its** members.

Currently, the following cannot be taken over:

- private messages/direct messages
- channels with end-to-end encryption
- bot accounts and settings for bot integrations


## Migration tool

You can initiate the migration of rooms at [migrate.chat.gwdg.de](https://migrate.chat.gwdg.de). You can select the rooms you want to migrate and then start the migration. 

![Migration tool](/images/70_Migration_01_de.png)



![Migration-Tool-2](/images/70_Migration_02_de.png)

When the migration is started, the migration bot is added to the channel.
After a successful migration, a final message is generated in the Rocket.Chat channel that links to the migrated channel in the matrix.
![Migrated channel in RC](/images/70_Migration_03_de.png)


## Failed migration

In rare cases, a migration that has already begun may fail. In this case, the migration will be stopped and you will be informed about it in the migration portal. Despite the error, the chat on Rocket.Chat is still usable. Failed migrations are regularly checked by the GWDG. They try to fix the errors and then restart the migrations. If a migration has not been completed even after a long period of time, please contact <a href=‘mailto:support@gwdg.de’>support(at)gwdg.de</a>.