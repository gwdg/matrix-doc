---
title: "Schlüsselverwaltung"
date: 2024-08-08T16:49:12+02:00
chapter: false
draft: false
weight: 2
---

## Schlüsselsicherung der Ende-zu-Ende-Verschlüsselung (E2EE) ##

Matrix nutzt grundsätzlich Transportverschlüsselung für alle Nachrichten von und zu Ihrem Heimserver (im Rechenzentrum der GWDG), aber ermöglicht auch die Nutzung von Ende-zu-Ende-Verschlüsselung (E2EE). Hierzu müssen kryptografische Schlüssel zwischen allen Geräten ausgetauscht werden, von denen sich Nutzer Ende-zu-Ende-verschlüsselt schreiben möchten. Obwohl diese technische Notwendigkeit kompliziert klingt (und es im Hintergrund auch wirklich ist), ist sie für die Anwendenden sehr bequem geworden. Die kryptografischen Schlüssel werden vom Client erstellt und auf dem jeweiligen Gerät gespeichert.

Sollte dies aber bspw. ein Tab in einem Browser sein, besteht die Gefahr, dass dieser Tab unbeabsichtigt geschlossen wird. Dann sind **durch den Verlust der Schlüssel auch alle verschlüsselten Nachrichten nicht mehr lesbar** und auch durch einen Administrator nicht wieder herstellbar. 
Damit dies nicht geschieht, bietet Element eine Schlüsselsicherung auf dem Heimserver an, in der alle kryptografischen Schlüssel abgelegt sind.

{{% notice warning %}}
Wir raten dringend dazu, die Schlüsselsicherung zu nutzen. Bei Verlust aller Schlüsselkopien sind verschlüsselte Chats sonst nicht mehr lesbar.
{{% /notice %}}

Falls Sie bereits an einem Raum teilnehmen, werden Sie durch einen Dialog zur Sicherung Ihrer Schlüssel aufgefordert. Sonst finden Sie den Punkt unter "Sicherheit" in Ihren Accounteinstellungen.

![Sicherheit im Menue](/images/07_Browser_Menue_Sicherheit_de.png)

Wählen Sie "Sicherheit" -> "Verschlüsselung" -> "Verschlüsselte Sicherung" und klicken Sie den Button "Einrichten".
Falls Sie im Laufe des Vorgangs außerhalb des Dialogs klicken, schließt sich dieses Unterfenster. Sie können es aber jederzeit wieder über den Eintrag in "Sicherheit" aufrufen.

![Security & Privacy](/images/08_Browser_Security_Privacy_de.png)

Wählen Sie, ob Sie für Ihren Sicherheitsschlüssel eine selbstgewählte Sicherheitsphrase eingeben möchten oder ob ein zufälliger Schlüssel generiert werden soll.

![Auswahl Sicherheitsschlüssel oder -phrase](/images/09_Browser_Schluesselsicherung_einrichten_de.png)

{{% notice warning %}}
Nutzen sie auf keinen Fall das Passwort Ihrer Academic ID oder anderer Zugangsdaten.
{{% /notice %}}

![Sicherheitssphrase eingeben](/images/10_Browser_Sicherungsphrase_eingeben_de.png)

Legen Sie diesen Sicherheitsschlüssel sicher ab, z.B. in Ihrem Passwortmanager oder als Ausdruck.

![Sicherheitsschlüssel](/images/11_Browser_Sicherungsschluessel_speichern_de.png)

Sie haben Ihren Schlüssel erfolgreich gesichert.

![Verschlüsselte Sicherung erfolgreich](/images/12_Browser_Sicherungsschluessel_abgeschlossen_de.png)
