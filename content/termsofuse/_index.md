---
title: "Nutzungsbedingungen"
date: 2024-02-16T14:00:00+01:00
draft: false
chapter: false
---

Diese Nutzungsbedingungen treten ab dem 08.08.2024 in Kraft.

## Löschfristen

### Hinweise zur Föderation

{{% notice note %}}
Daten bzw. Dateien, die auf anderen Matrix-Servern liegen, können von der GWDG nicht gelöscht werden. Über die Föderation ist es Angehörigen der GWDG Matrix Server möglich, Räume externer Matrix-Server zu betreten und umgekehrt. In diesem Fall hält der externe Server ebenfalls Daten und Dateien der GWDG-Matrix-Server bereit, handhabt das Löschen dieser Informationen ggf. anders. Weiterhin ist es möglich, dass Daten noch im temporären Zwischenspeicher von Matrix-Clients der Nutzer:innen vorhanden sind.
{{% /notice %}}

### Dateien

Matrix lässt sich zum Austausch von Dateien verwenden, ist aber nicht als längerfristigere Aufbewahrung gedacht. Aus diesem Grund werden Dateien, die in Matrix empfangen bzw. verschickt wurden, nach einer gewissen Zeit automatisiert von den  Matrix-Servern der GWDG entfernt. Konkret wird eine Datei 12 Monate, nachdem der letzte Zugriff auf sie erfolgte, gelöscht.

{{% notice tip %}}
Zur dauerhaften Aufbewahrung von Dateien können entsprechende Dienste wie bspw. [ownCloud](https://owncloud.gwdg.de) genutzt werden.
{{% /notice %}}

### Sitzungen

Sitzungen, die seit mehr als 120 Tagen nicht mehr genutzt wurden, werden automatisch gelöscht. Es erfolgt also eine Abmeldung aus dem jeweils genutzten Matrix-Client.

{{% notice info %}}
Wenn Sie sich in einem Matrix-Client wie bspw. Element anmelden, entsteht eine Sitzung. Durch das Abmelden aus einer Sitzung wird diese gelöscht. Sitzungen können bspw. in Element über die „Einstellungen“ - „Sitzungen“ eingesehen werden. In dieser Ansicht werden inaktive Sitzungen, also länger nicht genutzte, separat aufgelistet und können bei Bedarf entfernt werden.
{{% /notice %}}

{{% notice tip %}}
Generell sollten Sie sich nur aus einer Sitzung abmelden, wenn die „Verschlüsselte Sicherung“ eingeschaltet ist bzw. vor der Abmeldung die „E2E-Raumschlüssel“ exportiert wurden und mindestens eine weitere vorhanden ist. So ist gewährleistet, dass der Zugriff auf verschlüsselte Nachrichten weiterhin möglich ist.
{{% /notice %}}

### Matrix-Konten

#### Bei inaktiver Academic ID

Wenn die Academic ID abgelaufen ist, werden vorhandene Sitzungen gelöscht. Es erfolgt also eine Abmeldung aus allen genutzten Matrix-Clients. Ein Zugriff auf das Matrix-Konto ist mit einem abgelaufenen Academic ID Login nicht möglich. 

Sollte das Academic ID innerhalb von 15 Monaten reaktiviert werden, ist der Zugriff auf das Matrix-Konto wieder möglich. Dabei kann es allerdings zu Einschränkungen beim Zugriff auf verschlüsselte Nachrichten kommen:

* Der Zugriff auf während der Inaktivität empfangene verschlüsselte Nachrichten ist nicht möglich.
* Ein Zugriff auf ältere verschlüsselte Nachrichten ist nur möglich, wenn entweder
  * die „Verschlüsselte Sicherung“ aktiv und deren Sicherheitsschlüssel bzw. -phrase bekannt ist oder
  * die „E2E-Raumschlüssel“ vor Ablauf der Academic ID exportiert wurden.


#### Bei gesperrter Academic ID

Wenn das ZIH-Login seit mehr als 15 Monaten abgelaufen ist, wird das zugehörige Matrix-Konto deaktiviert.

Folgende Daten des Matrix-Kontos werden u.a. gelöscht:

* Mitgliedschaften in allen Räumen
* alle Sitzungen
* alle E2EE-Schlüssel
* die „Verschlüsselte Sicherung“
* Anzeigename
* Profilbild
* Blockliste

Nicht gelöscht werden folgende Daten:

* hochgeladene Dateien
* verschickte und empfangene Nachrichten
