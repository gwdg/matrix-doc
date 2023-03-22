---
title: "Nachrichten"
date: 2020-07-15T18:10:07+02:00
draft: false
chapter: true
weight: 30
---

## Personen finden und direkte Nachrichten versenden

Um einzelne Personen anzuschreiben und somit einen privaten 1:1 Chat zu erzeugen, klickt man zunächst auf das + in der Kategorie „Direkte Nachrichten“:

![Klick au den Chat starten Button](/images/01_Start-Chat_de.png)

Nun kann in das Suchfeld die Matrix-Adresse der Person eingeben werden, die man erreichen möchte. Nach dem letzten eingegebenen Zeichen sollten Sie bis zu fünf Sekunden warten, bis die Sucherergebnisse vollständig angezeigt werden. Beachten Sie auch, auf welchem Server Ihre gesuchte Person angezeit wird

Beachten Sie, dass aus Datenschutzgründen nur Personen in der Suche erscheinen, mit denen Sie sich bereits in einem gemeinsamen Raum befinden. Sie können jedoch einfach auf **Los** klicken. Wenn die Matrix-Adresse korrekt ist, wird der Gesprächsteilnehmende dennoch zu einem 1:1 Chat eingeladen (auch wenn nicht in der Suche angezeit).

{{% notice note %}}
Ein Einfügen von Matrix-Adressen (bspw. via `strg+v`) reicht nicht aus, um Personen zu finden! Am besten geben Sie die Zeichen der Matrix-Adresse per Hand ein (Zeichen für Zeichen).
{{% /notice %}}

Wenn Sie niemanden finden können, fragen Sie nach deren Benutzernamen oder teilen Sie ihren Benutzernamen (`@<tu_login>:matrix.tu-berlin.de`) oder https://matrix.to/#/@tu_login:matrix.tu-berlin.de, damit die angesprochene Person Sie innerhalb von Matrix kontaktieren kann. Eine Einladungs-E-Mail wird nicht durch Matrix versendet.

![Ergebnis zugefügt zu den Personen, die in den Chat eingeladen werden](/images/02_Start-Chat_de.png)

<!--
Beachten Sie, dass Matrix-Accounts von ZIH-Funktionslogins möglicherweise nicht geprüft werden. Aufgrund der Neuheit des Mediums für Viele sowie der fehlenden Multi-Account-Funktionalität vom Matrix-Client Element, werden TU Dresden Mitarbeitende womöglich eher ihren persönlichen ZIH-Login nutzen.
-->

Es öffnet sich das [Ende-zu-Ende-verschlüsselte]({{< relref "encryption" >}}) (inzwischen Standard) Gespräch, welches nach Annahme der Einladung durch die verbundene Person beginnen kann. Die Verbindung zum Server an der TU Dresden ist natürlich auch transport-verschlüsselt. Sollten Sie aus einem speziellen Grund explizit keine Ende-zu-Ende-Verschlüsselung wünschen, wäre ein unverschlüsselter [Raum zu erzeugen]({{< relref "rooms/create.md" >}}) und die Gesprächspartner:in in diesen einzuladen.

### Einladen von Personengruppen

Für das Einladen von mehreren Personen (bis zu 100 auf einmal, dann wiederholbar) müssen die Matrix-Adressen in der Form `@ZIH-Login:tu-dresden.de` vorliegen. Diese können Sie beispielsweise in einem Texteditor Zeile für Zeile sammeln und dann mittels Zwischenablage (Kopieren & Einfügen) in das Suchfeld in Matrix/Element einfügen.

### Raum als Zwischenablage verwenden

Es ist möglich einen Raum mit sich selbst zu erstellen. In diesem Raum ist man also der einzige Teilnehmer. Dieser Raum kann dann als Zwischenablage / Notizbuch sowie für Tests benutzt werden, zum Beispiel um zu prüfen ob Formatierungen (zum Beispiel von Latex) und Hyperlinks korrekt funktionieren.

### Weiteres
* [Nachrichten formatieren]({{< relref "formatting.md" >}})
* [Nachrichten suchen]({{< relref "search.md" >}})
