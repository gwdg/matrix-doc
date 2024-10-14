---
title: "Migration"
date: 2024-09-26T13:45:15+02:00
draft: false
chapter: false
weight: 70
---
## Ende von chat.gwdg.de

Rocket.Chat bleibt auch nach dem September 2024 weiter verfügbar, allerdings läuft die Lizenz kurz vor Ende September aus. Ab diesem Zeitpunkt wird es folgende Einschränkungen geben:

- Mobil-Clients erhalten keine Push-Benachrichtigungen mehr
- der Online-Status von Accounts (anwesend/abwesend/beschäftigt/offline) ist nicht mehr sichtbar

Wann die Verfügbarkeit von Rocket.Chat final endet ist noch nicht entschieden und wird auch von der Nutzung über den Zeitpunkt der Ablösung hinaus abhängig sein. Ziel ist es, jeder BenutzerIn genügend Zeit für den Wechsel einzuräumen und Arbeitsabläufe umstellen zu können. Allen BenutzerInnen wird die Umstellung empfohlen.

## Migration zu Matrix

Mit [migrate.chat.gwdg.de](https://migrate.chat.gwdg.de) wird eine Webseite zur Verfügung gestellt, die ein Umzug von Kanälen zu Matrix erlaubt, bei denen Sie die Rolle “Besitzer” haben. Die gesamte Historie inklusive Dateien wird dabei kopiert, der ursprüngliche Kanal auf Nur-Lesen gestellt und eine letzte, entsprechende Nachricht in dem Kanal eingestellt. Dieser Kanal wird für **alle** Mitglieder nach Matrix migriert.

Aktuell können nicht übernommen werden:

- private Nachrichten/Direkt-Nachrichten
- Kanäle mit Ende-zu-Ende-Verschlüsselung
- Bot-Accounts und Einstellungen zu Bot-Integrationen


## Migration-Tool

Auf [migrate.chat.gwdg.de](https://migrate.chat.gwdg.de) können Sie die Migration für Räume anstoßen. Zu migrierende Räume lassen sich auswählen und im Anschluss die Migration starten. 

![Migration-Tool](/images/70_Migration_01_de.png)



![Migration-Tool-2](/images/70_Migration_02_de.png)

Beim Start der Migration  wird der Migrations Bot dem Kanal hinzugefügt.
Nach erfogreicher Migration wird Rocket.Chat Kanal eine letzte Nachricht erzeugt die zum migrierten Channel in Matrix verlinkt.
![Migrierter Channel im RC](/images/70_Migration_03_de.png)


## Fehlgeschlagene Migration

In seltenen Fällen kann eine begonnene Migration fehlschlagen. In diesem Fall wird die Migration gestoppt und Sie werden im Migrationsportal darüber informiert. Der Chat auf Rocket.Chat ist trotz des Fehlers weiterhin nutzbar. Gescheiterte Migrationen werden von der GWDG regelmäßig überprüft. Es wird versucht, die Fehler zu beheben und die Migrationen anschließend erneut zu starten. Sollten eine Migration auch nach längerer Zeit nicht abgeschlossen sein, melden Sie sich bitte bei <a href="mailto:support@gwdg.de">support(at)gwdg.de</a>
