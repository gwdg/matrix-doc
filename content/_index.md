---
title: "Matrix in der Academic Cloud"
date: 2024-08-07T21:26:25+02:00
chapter: false
draft: false
---

<!--## Wartungsarbeiten am Montag den 06.11.23 ab 20:30 Uhr

Am Montag den 06.11.23 ab 20:30 Uhr finden Wartungsarbeiten statt - Matrix wird voraussichtlich für einige Stunden nicht erreichbar sein.-->

## Element-Client

Unser Matrix-Homeserver ist über den [Element-Client](https://chat.academiccloud.de/) im Browser erreichbar.


{{% notice info %}}
Denken Sie bitte an die [Einrichtung der Schlüsselsicherung]({{% relref "encryption/keymanagement/_index.md" %}})!
{{% /notice %}}

## Dokumentation im Aufbau
Aktuell arbeiten wir noch daran die [Dokumentation von der TU-Dresden](https://doc.matrix.tu-dresden.de/) an unsere Matrix-Instanz anzupassen. Im Menü auf der linken Seite werden nach und nach immer mehr Seiten entstehen.

## Matrix in der Academic Cloud
Matrix ist ein freies und offenes, sicheres, dezentralisiertes Protokoll für Echtzeit-Kommunikation, das auch unter dem Namen eines seiner nutzenden Programme, Element, bekannt ist.

<object data="/images/matrix_interactive.svg" type="image/svg+xml" style="width: 1280px; max-width: 100%"></object>

Zur Zusammenarbeit in Teams stieg in den letzten Jahren der Bedarf an unterstützenden digitalen Werkzeugen. Ein zentrales Werkzeug ist dabei ein Team-Chat. Ein Chat bezeichnet, laut Wikipedia, „die elektronische Kommunikation mittels geschriebenem Text in Echtzeit, meist über das Internet“ ([Quelle](https://de.wikipedia.org/wiki/Chat)). Mit einem Messenger (die Software zum Chatten) können sich Teammitglieder gegenseitig auf aktuelle Informationen aufmerksam machen und insbesondere Verknüpfungen (*Hyperlinks* / *Links*) zur weitergehenden Zusammenarbeit teilen (beispielsweise zur Terminfindung, zum kollaborativen Schreiben, zum Planen von Events, zum Bearbeiten von Daten, Code, Mindmaps oder Prozessen). Viele Teams in der Academic Cloud haben sich aufgrund des bisher fehlenden zentralen Angebots eigene Lösungen gesucht, die zum Teil datenschutzbedenklich sind oder nicht mit anderen Systemen verknüpfbar sind.

Zur Deckung des Bedarfes an Echtzeitkommunikation wurde daher im August 2024, nach vergleichender Analyse mehrerer potentieller Lösungsoptionen, innerhalb der Academic Cloud das offene Kommunikationsprotokoll Matrix eingeführt. Zu Ende 2024 soll das bisherige Chat-System Rocket.Chat abgelöst werden.

<!--
<img id="image-id" style="width: 1280px; max-width: 100%; margin-left:0;">
<script>
var cssSelector = "#image-id";
var imageFolderPath = "/images/statements";
var imageCount = 19;
var displayTime = 30000; //in ms
document.querySelector(cssSelector).src = imageFolderPath+"/"+Math.floor(Math.random() * imageCount)+".jpg";
setInterval(() => {
    document.querySelector(cssSelector).src = imageFolderPath+"/"+Math.floor(Math.random() * imageCount)+".jpg";
}, displayTime);
</script>
-->

## Themen der Dokumentation

* [Warum Matrix und kein anderes Chat-System?]({{% relref "why/_index.md" %}})
* [Wie kann Matrix genutzt werden? (Anmeldung und erste Schritte)]({{% relref "first-steps/_index.md" %}})
* [Empfehlungen zu weiteren wichtigen Einstellungen nach dem Erstlogin]({{% relref "settings/_index.md" %}})
* [Matrix-Clients installieren und einrichten]({{% relref "clients/_index.md" %}})
    * [Element Web]({{% relref "clients/browser/_index.md" %}})
    * [Element Desktop]({{% relref "clients/desktop/_index.md" %}})
    * [Element Android]({{% relref "clients/android/_index.md" %}})
    * [Element iOS]({{% relref "clients/ios/_index.md" %}})
    * [Element-Installation unter Linux]({{% relref "clients/install_linux/_index.md" %}})
* [Personen finden und direkte Nachrichten versenden]({{% relref "messaging/_index.md" %}})
    * [Nachrichten formatieren]({{% relref "messaging/formatting/_index.md" %}})
    * [Nachrichten suchen]({{% relref "messaging/search/_index.md" %}})
* [Räume erstellen und Verantwortung übernehmen]({{% relref "rooms/_index.md" %}})
    * [Räume erstellen]({{% relref "rooms/create/_index.md" %}})
    * [Räume finden]({{% relref "rooms/find/_index.md" %}})
    * [Räume löschen und aus Räumen austreten]({{% relref "rooms/delete/_index.md" %}})
    * [Räume teilen und publik machen]({{% relref "rooms/sharing/_index.md" %}})
* [Benachrichtigungen feiner einstellen]({{% relref "notifications/_index.md" %}})
* [Spaces zur Raumverwaltung einsetzen]({{% relref "spaces/_index.md" %}})
* [Ende-zu-Ende-Verschlüsselung nutzen]({{% relref "encryption/_index.md" %}})
<!--
* [Integrations, Bridges, Bots nutzen (u.a. Jitsi)]({{% relref "integrations/_index.md" %}})
-->
* [Automatisierungen]({{% relref "automations/_index.md" %}})
* [Migration zu Matrix]({{% relref "migration/_index.md" %}})
* [Häufige Fragen (FAQ)]({{% relref "faq/_index.md" %}})
* [Weiterentwicklung von Matrix]({{% relref "development/_index.md" %}})
* [Impressum]({{% relref "imprint/_index.md" %}})
* [Datenschutzerklärung](https://gwdg.de/impress)

### Fragen / Kontakt

Allgemeine Fragen richten Sie bitte per Mail an das Ticketsystem der GWDG:
<a href="mailto:support@gwdg.de">support(at)gwdg.de</a>

Probleme und Lösungen können darüber hinaus durch Schildern des Sachverhalts gemeinsam im Matrix-Support-Raum [#general:gwdg.de](https://matrix.to/#/#general:gwdg.de) diskutiert werden, sodass alle Anderen durch den transparenten Austausch lernen können. Dort werden auch aktuelle Wartungen angekündigt.

{{% notice tip %}}
Man kann bei manchen Anomalien probieren den Cache (Zwischenspeicher) zu leeren und alles neu zu laden: Einstellungen > Hilfe & Über > Cache löschen und neu laden
{{% /notice %}}

{{% notice note %}}
Aktuelle Wartungen werden in dem Matrixraum [#general:gwdg.de](https://matrix.to/#/#general:gwdg.de) angekündigt.
{{% /notice %}}
