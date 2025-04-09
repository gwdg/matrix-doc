---
title: "Überprüfung"
date: 2025-04-09T12:47:03+02:00
chapter: false
draft: false
weight: 3
---

Bei der Anwendung von Matrix und Element für sensitiven Austausch ist eine möglichst vollständige Einrichtung der Verschlüsselung empfohlen.

Diese Seite gibt Hinweise darauf, wie die eigene Matrix *Security Posture* überprüft werden kann.

Hierfür betrachten wir Signierung der eingesetzten Schlüssel sowie deren verschlüsselte Sicherung.

> | Anwendungsbereich |
> |----|
> | Diese Anleitung wendet sich an Personen, die abhörsicher und vertraulich kommunizieren wollen oder müssen. |

Dies betrifft:

- die Verifizierung der eigenen Geräte
- die Verifizierung des Gegenübers
- die Sicherung des Exports der Verschlüsselungsschlüssel
- die Sicherung der Passphrase der Verschlüsselungsschlüssel

Im Verlauf behandeln wir diese einzeln.

&nbsp;

# Voraussetzungen

Zum Fortfahren benötigen wir:

- gründliches Lesen und Vertrautmachen mit der Matrix/Element-Dokumentation der AcademicCloud. Im weiteren Verlauf wird davon ausgegangen, dass diese Inhalte bekannt sind und dass die Schlüsselsicherung wie im Dokument **Wichtige Einstellungen** beschrieben aktiviert ist.  
  - Deutsch:  
    **[Wichtige Einstellungen](https://docs.chat.academiccloud.de/settings/index.html)**  
    [Verschlüsselung](https://docs.chat.academiccloud.de/encryption/index.html):  
    | Zitat |
    |----|
    | Zum aktuellen Zeitpunkt raten wir stark von einer Verschlüsselung von Räumen mit mehr als 4 oder 5 Teilnehmenden ab, da es sonst gehäuft zu nicht-Entschlüsselbaren Nachrichten bei einigen Personen kommen kann. |
  - Englisch:  
    **[Important settings](https://docs.chat.academiccloud.de/en/settings/index.html)**  
    [Encryption](https://docs.chat.academiccloud.de/en/encryption/index.html):  
    | Quote |
    |----|
    | We strongly discourage from enabling encryption for rooms with more then 5 people. Else you might see a lot of problems with undecryptable messages. |
- einen entsperrten persönlichen Schlüsselbund in einem Passwort-Manager zur Ablage von Zugangsdaten, Passphrasen und kryptographischen Schlüsseln

&nbsp;

# Problemstellung

In der Verwendung von Matrix und Element als Ende-zu-Ende-verschlüsselnden Messenger stellt sich wie in allen kryptographischen Systemen die Frage nach der sicheren Ablage und Übertragung der zu verwendenden Schlüsselpaare (öffentlich/privat). Da Matrix ähnlich dem Signal-Protokoll häufig die Schlüssel automatisiert wechselt, kommt eine Kaskade von kryptographischen Signaturen und Verifikationen zum Einsatz, um dies zu erlauben. Anders als bei Signal sollen diese Verfahren auch in selbstbetriebenen Umgebungen und im Webbrowser sowie mit einer Vielzahl von Clients auf verschiedenen Geräten bei Sender wie Empfänger der Nachrichten funktionieren.

Mehrere Dinge treffen hier auf einander:

- Die Verteilung der öffentlichen Schlüssel an Kommunikationspartner (trivial, da öffentlich)
- Die Verteilung der privaten Schlüssel zwischen eigenen Geräten (involviert, da privat)
- Die Verifizierung der eigenen Geräte (moderat, da selbstgesteuert)
- Die Verifizierung der Geräte der Kommunikationspartner (involviert, da interaktiv)

Manche dieser Dinge bauen aufeinander auf (eigene Verifizierung \> private Schlüssel austauschen \> mit anderen verschlüsselt kommunizieren) oder sind Voraussetzung für einen sicheren Betrieb der Verschlüsselungsinfrastruktur (Verifizierung der eigenen und der Geräte anderer).

> | Voraussetzung |
> |----|
> | Eine vollständige und in ihrer Funktion überprüfte sowie bestätigte Einrichtung der Matrix/Element-Verschlüsselung ist Voraussetzung für den sicheren verschlüsselten Austausch. |

Der Hersteller gibt uns mehrere Werkzeuge an die Hand, um die Verschlüsselungsaspekte möglichst unbesehen im Hintergrund stattfinden zu lassen.

&nbsp;

> &nbsp;
>
> > **Wie können wir sicherstellen, dass unsere Matrix/Element-Kommunikation vertrauenswürdig und sicher ist?**
>
> &nbsp;

&nbsp;

# Lösungswege

Die Verschlüsselung von Matrix/Element arbeitet auf zwei Ebenen:

1. Zur Verifizierung der Authentizität der Übertragung werden Nachrichten mit dem jeweils aktuellen privaten Schlüssel digital signiert. Diese Signatur kann kryptographisch im Abgleich mit bekannten, aktuell gültigen öffentlichen Schlüsseln überprüft werden.
2. Zur Aufrechterhaltung der Integrität privater Nachrichten werden diese mit den jeweils aktuellen öffentlichen Schlüsseln verschlüsselt, versandt und auf Empfängerseite mit den jeweils aktuellen privaten Schlüsseln entschlüsselt.

> | Hintergrund |
> | --- |
> | Die Verwendung jeweils nur aktueller Schlüssel bedeuet, dass diese analog des Signal-Protokolls regelmäßig rotiert werden, sodass mit neueren Schlüsseln keine Entschlüsselung älterer Nachrichten mehr möglich ist, was das Risiko bei einer Kompromittierung verringert. Diese Eigenschaft wird Perfect Forward Secrecy genannt.<br /><br />Hieraus ergibt sich, dass mit der Zeit der Schlüsselspeicher kontinuierlich anwächst. Bei aktivierter Schlüsselsicherung können neu eingeloggte Geräte nach gegenseitiger Verifizierung auch ältere Schlüssel nachladen. Dadurch können sie auch ältere Nachrichten entschlüsseln die gesendet wurden, als sie noch nicht angemeldet waren.<br /><br />Das bedeutet auch, das ein manueller Export der Raumschlüssel ausschließlich Nachrichten entschlüsseln kann, die vor dem Export verarbeitet wurden. Für neuere Nachrichten würden sehr bald durch die beständige Rotation neue Schlüssel zum Einsatz kommen. |

Kür und Hürde liegen darin:

- sich mit seinen eigenen Geräten und gegenseitig mit den Kommunikationspartnerïnnen zu verifizieren, um die Authentizität des Gegenübers zu bestätigen.
- die privaten Verschlüsselungsschlüssel beständig zwischen den eigenen Geräten auszutauschen und die Kopien aktuell zu halten, um barrierefrei vertraulich zu chatten.

&nbsp;

## Verifizierung der eigenen Geräte

Das gegenseitige Verifizieren von Geräten (Login Sessions, Apps) nach der Erstanmeldung erlaubt den Schlüsselaustausch zwischen eigenen Geräten und die Aktivierung des Schlüsselbackups ohne Eingabe der Passphrase.

Eigene Sitzungen lassen sich überprüfen **(Abbildungen 10. ff.)** und ggf. nachverifizieren, während beide Geräte gleichzeitig eingeloggt und online sind.

Bei Erfolg der Einrichtung bestätigt dies die Ansicht der Sicherheitseinstellungen unter der Überschrift Quersignierung **(Abbildung 5.)**.

&nbsp;

## Verifizierung des Gegenübers

Die Verifizierung eines Gegenübers erlaubt die gegenseitige Quersignierung zur aktiven Bestätigung der beiderseitigen kryptographischen Identitäten.

**Abbildungsserie 9.**

Dies eröffnet für besondere Anwendungsfälle und Bedrohungsszenarien die Möglichkeit eines höheren Sicherheitsniveaus.

&nbsp;

## Sicherung des Exports der Verschlüsselungsschlüssel

Die Verschlüsselungsschlüssel der Räume (Raumschlüssel) lassen sich manuell mit einem Export als `element-keys.txt` im persönlichen Schlüsselbund abspeichern.

Dadurch eröffnet sich ein zusätzlicher Wiederherstellungspfad für die kryptographischen Schlüssel.

Für den Export ist die Eingabe der Verschlüsselungspassphrase der verschlüsselten Schlüssel nötig.

**(Abbildungen 4. + 6)**

Die Exporte im Schlüsselbund sind in persönlich angemessener Kadenz aktuell zu halten.

&nbsp;

## Sicherung der Passphrase der Verschlüsselungsschlüssel

Wenn die Schlüsselsicherung aktiviert ist, erscheint dies in den Einstellungen **(Abbildung 3.)**.

Es ist zu prüfen, dass bei aktiviertem Schlüsselbackup auf dem Matrix-Server der Element Security Key (`security-key.txt`)

\(1\) im persönlichen Schlüsselbund vorliegt und

\(2\) dass diese Kopie der Verschlüsselungspassphrase für das Schlüsselbackup auch funktioniert.

Das lässt sich mit einem Export der Verschlüsselungsschlüssel oder im Zuge der Anmeldung an einem anderen Gerät / in einer anderen Matrix-App testen.

&nbsp;

# Erhöhung der Sicherheit

Zur Erhöhung der Sicherheit können für bestimmte Anwendungsszenarien weitere Vorkehrungen getroffen werden.

&nbsp;

- **Warnungen beachten (Abbildung 8.)**  
  Element informiert einen über zurückgestellte oder fehlende Verschlüsselungssicherheit.  
  In besonderen Fällen, wenn Kommunikationspartner ihre eigenen Geräte nicht verifiziert haben, erscheinen Warnmeldungen, welche den Bruch der Kette der Integritätsprüfungen signalisiert.  
  Dies kann im persönlichen Gespräch unter Erwähnung dieser Seite im Wiki Beachtung finden und mit Screenshots untermauert werden.  
  *In solchen Fällen, in denen für sicherheitsrelevante Kommunikation ein bestimmtes Sicherungsniveau vorausgesetzt wird, ist solch eine Situation mit Hilfe Dritter aufzulösen.*

&nbsp;

- **Verschlüsselte Nachrichten nur an verifizierte Sitzungen senden (Abbildung 7.)**  
  Für die Erhöhung des Allgemeinen Schutzniveaus lässt sich einstellen, dass Nachrichten nur an Kommunikationspartner geschickt werden, welche die Sitzungen auf ihren Geräten verifiziert haben.  
  Dies unterbindet die Kommunikation mit nicht-verifizierten Geräten und kann Ausschlüsse verursachen, bspw. wenn gar keine verifizierte Sitzung vorliegt und Nachrichten nirgends zugestellt werden können.

&nbsp;

# Bekannte Probleme

- Die Schlüsselsicherung ist nicht aktiviert
  - Schlüsselsicherung aktivieren
- Die Passphrase für die Schlüsselsicherung wurde vergessen zu notieren oder zu sichern  
  - Schlüsselsicherung zurücksetzen
- `element-keys.txt` ist nicht im Schlüsselbund gespeichert
  - `element-keys.txt` nach dem Download im Download-Ordner wiederfinden und als Anhang zusammen im selben Eintrag mit der Sicherheitspassphrase der Schlüsselsicherung  (`security-key.txt`) speichern.
  - Ggf. aus dem Download-Ordner löschen, wenn keine Festplattenverschlüsselung zum Einsatz kommt.
- `security-key.txt` mit der Sicherheitspassphrase der Schlüsselsicherung ist nicht im Schlüsselbund gespeichert
  - `security-key.txt` nach dem Download im Download-Ordner wiederfinden und dann als Anhang zusammen im selben Eintrag mit den exportierten Raumschlüsseln (`element-keys.txt`) speichern.
  - Ggf. aus dem Download-Ordner löschen, wenn keine Festplattenverschlüsselung zum Einsatz kommt.

&nbsp;

# Abbildungen

&nbsp;

1.  **Die Sicherheitseinstellungen öffnen**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-1.png)  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-2.png)  
      
      
2.  **Die Verschlüsselungseinstellungen in den Sicherheitseinstellungen finden**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-3.png)  
      
      
3.  **Die Verschlüsselte Sicherung bestätigen**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-4.png)  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-5.png)  
      
      
4.  **Die Quersignierung und Verschlüsselung (erneut) weiter unten vorfinden**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-6.png)  
      
      
5.  **Die Quersignierung bestätigen**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-7.png)  
      
      
6.  **Die Ende-zu-Ende-Raumschlüssel exportieren**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-8.png)  
      
      
7.  **Erhöhtes Sicherheitsniveau verwenden**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-9.png)  
      
      
8.  **Warnungen beachten**  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-10.png)  
      
      
9.  **Sich gegenseitig verifizieren  
    **nur bei gleichzeitig bestehendem zweiten Kommunikationskanal anzustoßen  
      
            **Variante A:** Das Profil des Gegenübers mit Klick auf das Avataricon im Chat zur rechten Bildschirmseite öffnen  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-11.png)  
      
            **Variante B:** Das Profil aus der Liste der im Raum anwesenden Personen heraus öffnen  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-12.png)  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-13.png)  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-14.png)  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-15.png)  
      
            ![](/images/content/encryption/validation/matrix-sicherheit-16.png)  
      
    Den Verifizierungsvorgang beginnen, während mensch zusammen sitzt oder telefoniert  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-17.png)  
      
      
10. **Sitzungen überprüfen**  
      
    Die Liste der Sitzungen lässt sich ausklappen  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-18.png)  
      
      
    In der sich öffnenden Liste lassen sich einzelne Sitzungen zur eingehenden Überprüfung per Klick öffnen  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-19.png)  
      
      
    Die sich öffnende Ansicht erlaubt es den Status der Verifizierung anzuzeigen und diese nur für jenes Gerät des Gegenübers anzustoßen  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-20.png)  
      
      
    Auf einem verifizierten Profil mit verifizierten Geräten erscheinen die Sitzungen anders  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-21.png)  
      
    Es erscheinen nun grüne Bestätigungsschilder mit Häkchen und die Sitzungen werden als vertrauenswürdig bestätigt dargestellt.  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-22.png)  
      
      
    Von hier aus lassen sich auch die eigenen Sitzungen anzeigen und überprüfen.  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-23.png)  
      
      
    ![](/images/content/encryption/validation/matrix-sicherheit-24.png)  
      
      
    Dieser Bildschirm ist auch über das Einstellungsmenü oben links erreichbar  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-25.png)  
      
    ![](/images/content/encryption/validation/matrix-sicherheit-26.png)

&nbsp;

Sicherer Kommunikation mit Matrix und Element steht nun nichts mehr im Wege!

&nbsp;

Glückwunsch und Dank für den geleisteten Einsatz für vertrauliche Kommunikation in sensiblen Belangen.

&nbsp;
