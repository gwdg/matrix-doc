---
title: "Wichtige Einstellungen"
date: 2020-07-03T13:22:13+02:00
draft: false
chapter: true
weight: 10
---
# Empfehlungen zu Schritten nach dem Erstlogin

## Einrichtung der Schlüsselsicherung

Matrix verschlüsselt nicht nur die Daten zwischen den Clients und dem Homeserver (im Rechenzentrum der TU Berlin) sondern erlaubt auch die Nutzung von Ende-zu-Ende-Verschlüsselung (E2EE). Hierzu müssen kryptografische Schlüssel zwischen allen beteiligten Geräten ausgetauscht werden. Obwohl diese technische Notwendigkeit kompliziert klingt und im Hintergrund auch ist, ist sie inzwischen für die Anwendenden sehr bequem geworden. Die vielen kryptografischen Schlüssel werden vom Client erstellt auf dem jeweiligen Gerät gespeichert. Sollte dies beispielsweise ein Tab in einem Browser sein, besteht die Gefahr, dass dieser Tab einmal unbeabsichtigt geschlossen wird. Dann sind verschlüsselten Inhalte unter Umständen nicht mehr lesbar. Damit dies nicht geschieht, wird eine Schlüsselsicherung auf dem Homeserver der TU Berlin angeboten, auf der (mit einer Sicherheitsphrase bzw. daraus errechenbaren Sicherheitsschlüssel geschützt) alle kryptografischen Schlüssel (verschlüsselt) abgelegt sind.

{{% notice info %}}
Es wird dringend empfohlen, die Schlüsselsicherung zu nutzen. Die Sicherheitsphrase, darf **nicht** Ihrem TUB-Passwort entsprechen!
{{% /notice %}}

![Aufforderung den Sicherheitsschlüssel zu generieren oder eine Sicherheitsphrase einzugeben](/images/11_Setup-Key_de.png)
![Aufforderung eine Passwort für die Schlüsselsicherung einzugeben](/images/12_Enter-Key_de.png)

Alternativ können Sie sich statt der Sicherheitsphrase auch einen Sicherheitsschlüssel generieren lassen, welcher den selben Zweck wie die Sicherheitsphrase erfüllt. Weiterhin wird der Sicherheitsschlüssel immer zusätzlich zur Sicherheitsphrase erstellt und sollte als Notfallschlüssel sicher und wiederauffindbar verwahrt werden (z.B. Abspeichern als .txt-Datei und Ausdrucken).

![Anzeige des Sicherheitsschlüssel zum abschreiben oder wegspeichern](/images/13_Present-Key_de.png)

Meldet man sich nun von einem anderen Gerät beziehungsweise mit einem anderen Client an, wird man dazu aufgefordert die Sitzung zu verifizieren. Ist man noch mit einem weiteren Client angemeldet, kann die Verifikation über dieses Gerät erfolgen. Andernfalls ist man auf den Sicherheitsschlüssel oder die Sicherheitsphrase angewiesen.

![Screenshot der Aufforderung eine Sicherheitsphrase einzugeben](/images/01_Restore-Session_de.png)

Sollte die Schlüsselsicherung nicht eingerichtet worden sein, kann nach einer Abmeldung nicht auf verschlüsselte Nachrichten zugegriffen werden. Auch das Schließen eines Browser-Tabs kann unter ungünstigen Umständen zu einer Abmeldung des Clients vom Homeserver führen.

![Bestätigung des Überspringens der Eingabe einer Sicherheitsphrase](/images/03_Cancel-Restore_de.png)

Vermeiden Sie diese Situation durch eine eingerichtete Schlüsselsicherung!

## Weitere wichtige Einstellungen

Nach erfolgreicher Einrichtung der Schlüsselsicherung können Sie nun die Desktop-Benachrichtigungen aktivieren.
Dies kann später auch rückgängig gemacht werden und insbendore können die Benachrichtigungen für einzelne „Gespräche“ (Räume) eingestellt werden.

![Screenshot der Abfrage, Pushbenarchitigungen zu aktivieren](/images/06_Enable-Notifications_de.png)

Das **Einstellungsmenü** kann geöffnet werden indem auf das runde Anzeigebild oben Links und anschließend auf die Zeile "Alle Einstellungen" geklickt wird.

![Auswahl des Menüpunkts Einstellungen in dem Nutzer:innenmenü](/images/06_Settings_de.png)

In den Einstellungen können Sie im Reiter **Allgemein** bei Bedarf Ihren Anzeigenamen ändern („Vorname Nachname“) und ein Profilbild hochladen:
![Makierung des Feldes Anzeigenamen und des Profilbilds in den Einstellungen](/images/06_Settings-Names_de.png)

<!--Mittelfristig wird der Anzeigename aus dem Common Name im LDAP der TU Dresden erhalten, dann ist ein manuelles Ändern nicht mehr nötig.-->

Das E-Mail-Adressfeld ist nicht unbedingt zu füllen, da über Ihren TUB-Login eine E-Mail-Adresse hinterlegt ist. Theoretisch können hier weitere Adressen hinzugefügt werden, beispielsweise um Benachrichtigungen über verpasste Nachrichten an eine weitere E-Mail-Adresse senden zu lassen.

<!--Auf der selben Seite kann auch das Design Thema von hell zu dunkel verändert werden.-->

Im Reiter **Benachrichtigungen** können Sie E-Mail-Benachrichtigungen (um über verpasste Nachrichten informiert zu werden) sowie akustische Benachrichtigungen aktivieren und diese granular für einzelne Aktivitäten Anderer einstellen. Mehr dazu auf der Seite [Benachrichtigungen]({{< relref "notifications" >}}).

![Screenshot der Benarchrichtigungeneinstellungen mit einer Makierung der ausgeschalteten E-Mail benachrichtigungen](/images/06_Settings-EMailNotify_de.png)

Im Reiter **Anrufe** können Sie den Matrix-Client Element berechtigen Ihre Mediengeräte (Kamera + Mikrofon) zu nutzen sowie Sprach-/Videoanrufe mittels direkter Peer-to-Peer-Verbindungen erlauben:

![Screenshot des Einstellungsmenüs Sprache und Video](/images/06_Settings-Media_de.png)

Erfreulicherweise starten 1:1 Gespräche standardmäßig Ende-zu-Ende-verschlüsselt. Um dieser Verschlüsselung wirklich mit gutem Gefühl zu vertrauen, können Nutzer:innen den Schlüsselvergleich mit Gesprächspartner:innen durchführen. Damit dies dann auch für alle Geräte dieser Gesprächspartner:innen gilt, müssen Matrix-Nutzenden ihrerseits wiederum die Schlüssel all ihrer Geräte untereinander verifizieren (Fachbegriff: Cross-Signing). Unter Beachtung der nachfolgenden Hinweise kann dies alles sehr bequem geschehen.

## Sicherheit & Datenschutz
Im Reiter **Sicherheit & Datenschutz** finden Sie alle Ihre Geräte, die bisher vom Matrix-Account genutzt wurden.

Entfernen Sie ggf. nicht mehr benutzte Sitzungen durch Markierung der quadratischen Box am Zeilenende und dem Klick auf den sich dann zeigenden roten Button.

![Screenshot des Menüs zum löschen von aktiven Sessions](/images/09_Delete-Sessions_de.png)

Die Geräte-Namen geben Ihnen auch Übersicht beim gegenseitigen Schlüsselvergleich zwischen Ihren Geräten.

Die hier vergebbaren öffentlichen Namen (durch Mausklick auf diese) Ihrer Geräte können auch von Gesprächspartner:innen eingesehen werden.  Dies hilft, wenn diese einen Vergleich der kryptografischen Schlüssel Ihrer Geräte (bspw. Laptop + Handy) durchzuführen möchten und so leicht die Gerätenamen identifizieren können.

Die vielen kryptografischen Schlüssel werden auf dem jeweiligen Gerät gespeichert. Sollte dies bspw. ein Tab in einem Browser sein, besteht die Gefahr, dass dieser Tab einmal unbeabsichtigt geschlossen wird. Dann sind alle verschlüsselten Inhalte nicht mehr lesbar. Damit dies nicht geschieht, wird eine Schlüsselsicherung auf dem Heimserver der TU Berlin angeboten, auf der (mit einer Passphrase geschützt) alle kryptografischen Schlüssel verschlüsselt abgelegt sind. Es wird dringend empfohlen, diese Schlüsselsicherung zu nutzen!

![Screenshot des Menüpunkts zur Schlüsselsicherung](/images/10_Setup-Keystore_de.png)
