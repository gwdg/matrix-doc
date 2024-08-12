---
menutitle: "Häufige Fragen (FAQ)"
title: "Häufige Fragen (FAQ)"
date: 2020-08-02T21:26:25+02:00
draft: false
weight: 200
---
Dies ist eine Zusammenstellung häufiger Fragen und deren Antworten.

- [Nachricht kann nicht entschlüsselt werden](#unable-to-decrypt)
- [Ich habe keinen Wiederherstellungsschlüssel](#no-recovery-key)
- [Wie ändere ich die Sicherheitsphrase für meine Schlüsselsicherung?](#change-securityphrase)
- [Wie kann ich die Schlüsselsicherung zurücksetzen, wenn ich meine Sicherheitsphrase UND meinen Sicherheitsschlüssel verloren habe?](#reset-securityphrase)
- [Was muss ich tun, wenn auf einem Mac oder MacBook Video oder Audio in einer Videokonferenz nicht funktioniert?](#apple-no-video)
- [Ich kann einen Kollegen/ Kommilitonen nicht einladen](#unable-to-invite)
- [Die Verbindung zum Server wurde unterbrochen](#no-connection)
- [Überall steht nur „missing translation: en“](#missing-translations)
- [Ist unser Server auf eurer Föderations-Blocklist?](#blocklist)
- [Ich sehe in einem Raum von einer bestimmten Person keine Nachrichten](#blocked-user)
- [Wie kann ich Matrix nutzen? / Ich finde keine Anleitung wie ich/andere Matrix nutzen können.](#how-to-login)
- [Ich habe mich an einem zweiten Gerät angemeldet und kann meine Nachrichten nicht lesen](#second-device-no-messages)
- [Ich habe Studien-/Forschungskollegen, die das auch nutzen wollen. Können die sich auch beim Academic Cloud Matrix anmelden? / Wie kann ich in Matrix mit Externen zusammenarbeiten?](#login-for-external-users)
- [Wie teilt man Leuten eine Raumadresse mit?](#share-room)
- [Wie kann ich als administrierende Person viele Nachrichten auf einmal löschen?](#delete-multiple-messages)
- [Manchmal sehe ich einen fett markierten Raum und klicke ihn an, habe aber doch nicht die Zeit, den Inhalt und etwaige Konsequenzen für mich sofort zu bearbeiten. Wie kann ich den Raum wieder als „ungelesen“ markieren?](#mark-room-as-unread)
- [Kann ich LaTeX schreiben?](#latex)
- [Gibt es so etwas wie Threads (vgl. Rocket.Chat/ Slack) in Matrix?](#threads)
- [Ich habe 2 Accounts, kann ich Nachrichten vom einen zum anderen weiterleiten lassen?](#forward-account)
- [Kann ich in Matrix Videokonferenzen veranstalten?](#videoconf-in-matrix)
- [Kann man über Matrix Dateien versenden? / Was ist die maximale Dateigröße, die über Matrix verschickt werden kann?](#file-upload)
- [Kann ich die/eine Matrix-App auf meinem Handy installieren, ohne Benachrichtigungen zu bekommen?](#app-without-notifications)
- [Ist es möglich, benachrichtigt zu werden wenn es neue Nachrichten in Matrix gibt, ohne eine App/Website zu öffnen?](#notifications-via-email)
- [Kann ich mit Element mehrere Matrix-Accounts verwalten (Multi-Account-Client)?](#multiple-accounts-element)
- [Wie kann ich einen (Chat-)Bot in Matrix bertreiben?](#hook)

***
# Problembehandlung / "Troubleshooting"

#### Nachricht kann nicht entschlüsselt werden {#unable-to-decrypt}
- **Tritt dies bei allen Nachrichten in einem Raum (bzw. allen Nachrichten in allen privaten Räumen) auf?**
  Die Anmeldung, in der die Nachrichten nicht sichtbar sind, wurde nicht verifiziert. Also:
    - Sicherheitsschlüssel oder Sicherheitspassphrase eingeben (diese wurden beim ersten Login festgelegt), oder
    - Diese Anmeldung interaktiv verifizieren (man vergleicht Emoji zwischen der ersten und der zweiten Anmeldung). Weitere Infos dazu gibt es [hier](/first-steps)
    - Schauen, ob die Einstellung "Niemals verschlüsselte Nachrichten von dieser Sitzung zu unverifizierten Sitzungen senden" aktiv ist. Diese Einstellung kann sowohl pro Anmeldung/Gerät als auch pro Raum gesetzt werden. Die Wirkung dieser Einstellung ist, dass unverifierte Gegenüber (a.k.a. mit welchen man noch keine Emojis ausgetauscht hat) die eigenen Nachrichten nicht mehr lesen können. Meist wird diese Einstellung bei der Ersteinrichtung von sicherheitsbewussten Anwendern reflexartig gesetzt, ohne, dass deren Konsequenzen vollumfänglich verstanden werden. Bei persönlich bekannten **und verifizierten** Gegenübern macht diese Einstellung durchaus Sinn und kann die Sicherheit erhöhen. Sofern man jedoch auch mit noch nicht verifierten / fremden Personen Nachrichten problemlos austauschen möchte (insbesondere in Gruppen), sollte man diese Einstellung mit Vorsicht und nur pro Raum setzen (bspw. bei Räumen mit besonders sensitiven Inhalten). Sicherheitsbewusste Anwender sollten mehr auf die Anzeige von grünen/roten Schilden neben Namen und roten Schilden neben Nachrichten vertrauen und achten.
- **Tritt dies nur bei Nachrichten in einem bestimmten Zeitraum auf?**
  Wahrscheinlich war in diesem Zeitraum kein Gerät mit dem Konto angemeldet. Um Matrix sicher zu nutzen, ist es *nicht* notwendig sich aus Sitzungen abzumelden (bspw. bevor man den Browser schließt), es wird daher empfohlen auf Geräten, die man wieder nutzen möchte, einfach angemeldet zu bleiben und die Webseite/Anwendung direkt zu schließen wenn gewünscht. So können, auch während kein Gerät angeschaltet ist, Nachrichten korrekt verschlüsselt und zugestellt werden.
  Falls Sie stets mit mindestens einem Gerät angemeldet waren, könnten auch die Einstellungen Ihres Browsers (sofern Sie Element im Browser verwenden) das Problem verursachen. Stellen Sie sicher, dass der Browser nicht selbstständig lokale Daten, Cookies o.ä. löscht.
- **Tritt dies vereinzelt / nur einmal auf?**
  Sie können zunächst nachschauen, ob es für Ihr Konto Anmeldungen gibt, die nicht verifiziert sind (dies findet sich in der Regel in Sicherheitseinstellungen der jeweiligen App oder Website), und den Sender der Nachricht aufforden, das selbe zu tun. Manchmal ist dieser Fehler nicht behebbar, in diesem Fall fordern Sie den Sender am besten auf, die Nachricht erneut zu veschicken.
***

#### Ich habe keinen Wiederherstellungsschlüssel {#no-recovery-key}
Bitte prüfen Sie, ob die Schlüsselsicherung eingerichtet wurde. Siehe [Schlüsselsicherung](/settings/#schlüsselsicherung).
***

#### Wie ändere ich die Sicherheitsphrase für meine Schlüsselsicherung? {#change-securityphrase}
- Bei allen Matrix-Sitzungen bis auf eine, auf die noch Zugriff besteht, die Raumschlüssel exportieren `Einstellungen`-> `Sicherheit & Datenschutz` -> `Verschlüsselung`. Abschließend abmelden, dafür links oben auf den Benutzernamen und abmelden, bei der Frage möglicherweise auftretenden Fage ob die verschüsselten Nachrichten gewünscht werden den Knopf `Ich möchte meine verschlüsselten Nachrichten nicht` betätigen, da diese Schlüssel eben schon exportiert wurden.
- Unter `Einstellungen`-> `Sicherheit & Datenschutz` -> `Sicheres Backup` erst den Knopf `Sicherung löschen`, dann den Knopf `Zurücksetzen`, möglicherweise ist ein löschen des Zwischenspeichers unter `Einstellungen`-> `Hilfe & Über` nötig, möglicherweise auch ein abmelden und erneutes anmelden mit anschließendem erneuten Versuch. Wenn das alles nicht geht, im nächsten Punkt fortfahren. Die Aktion war erfolgreich, wenn nur noch der grüne Einrichten Knopf angezeigt wird.
- Für alle vorher exportieren Schlüsselsicherungen den manuellen importweg ausführen.
- Neue Schlüsselsicherung einrichten. Siehe [Schlüsselsicherung](/settings/#schlüsselsicherung)
***

#### Wie kann ich die Schlüsselsicherung zurücksetzen, wenn ich meine Sicherheitsphrase UND meinen Sicherheitsschlüssel verloren habe? {#reset-securityphrase}
Bitte folgendes ausführen:
  1. In einer Matrix-Sitzung (=Client/Geräte/Browser), wo man die früheren verschlüsselten Gespräche noch lesen kann, die Raumschlüssel exportieren. Dazu zu unter `Einstellungen`-> `Sicherheit` -> `Verschlüsselung` auf E2E-Raumschlüssel exportieren klicken. Sollte es keinen Zugang zu irgendeiner Matrix-Sitzung mehr geben, in der frühere verschlüsselte Nachrichten lesbar sind, diesen Schritt überspringen.
  2. In der einen Matrix-Sitzung, bei der man soeben in Schritt 1 die Raumschlüssel manuell exportiert hat, unter `Einstellungen`-> `Sicherheit` -> `Verschlüsselung` alle weiteren Sitzungen am Zeilenende ankreuzen und unterhalb der Liste auf den rot umrandeten Knopf „x ausgewählte Geräte  abmelden“ klicken. Die oberste in Fettschrift ist die aktuelle Sitzung, diese nicht mit anhaken, also nicht löschen.
  3. Ggf. ausloggen und wieder einloggen, dabei Nachfragen ignorieren.
  4. Unter `Einstellungen`-> `Sicherheit` -> `Sicheres Backup` schauen ob dort ein grüner Knopf `Einrichten` und keine roten Knöpfe da sind. Oder wenn noch rote Knöpfe da sind, erst den Knopf `Sicherung löschen`, dann den Knopf `Zurücksetzen` klicken. Möglicherweise ist ein löschen des Zwischenspeichers (roter Knopf unter `Einstellungen`-> `Hilfe & Über`) nötig, möglicherweise auch ein Abmelden und erneutes Anmelden. 
  5. Anschließend unter `Einstellungen`-> `Sicherheit` -> `Quersignierung` auf den roten Knopf `Zurücksetzen` drücken. Die Aktion war erfolgreich, wenn für `Sicheres Backup` und `Quersignierung` nur noch der grüne Einrichten Knopf angezeigt wird.
  6. Jetzt die zuvor exportieren Schlüsselsicherungen manuell importieren. Dazu unter `Einstellungen`-> `Sicherheit` -> `Verschlüsselung` auf E2E-Raumschlüssel importieren klicken.
  7. Neue Schlüsselsicherung und Quersignierung einrichten mit den zwei grünen Knöpfen. Siehe [Schlüsselsicherung](/settings/#schlüsselsicherung). Den Sicherheitsschlüssel können Sie zum Beispiel ausdrucken und sicher verwahren.
***

#### Was muss ich tun, wenn auf einem Mac oder MacBook Video oder Audio in einer Videokonferenz nicht funktioniert? {#apple-no-video}
Häufig hat Element nicht die Rechte, auf die Webcam und das Mikrofon zuzugreifen. Diese können in den Systemeinstellungen unter Sicherheit und Privatsphäre vergeben werden.
***

#### Ich kann einen Kollegen/Kommilitonen nicht einladen {#unable-to-invite}
- Zunächst die Rechtschreibung prüfen (wurde das Kürzel oder der Name wirklich korrekt eingegeben?)
- Es ist nicht möglich, Nutzer mit ihrer E-Mail-Adresse einzuladen oder zu suchen. Am besten entweder das Kürzel (falls bekannt) suchen, oder "auf gut Glück" Vor- und/oder Nachnamen der Person suchen (dies geht nur, wenn die Person diese als Anzeigenamen gewählt hat)
- Nutzer können nur eingeladen werden, wenn diese sich mindestens einmal angemeldet haben. Falls das Kürzel / die Matrix-ID nicht gefunden werden kann, hat sich dieser Nutzer noch nie in Matrix angemeldet.
***

#### Die Verbindung zum Server wurde unterbrochen {#no-connection}
1. Hat Ihr Gerät Zugang zum Internet? Stellen Sie sicher, dass es sich nicht um ein Funkloch, ein ausgestecktes Internet-Kabel, o.ä. handelt.
2. Zur Wartung des Systems wird der Matrix-Server manchmal kurz neugestartet, in diesem Fall steht der Dienst nach wenigen Minuten wieder zur Verfügung.
***

#### Überall steht nur „missing translation: en“ {#missing-translations}
Dieses Phänomen steht häufig im Zusammenhang mit noch nicht fertiggestellten Aktualisierungen des Matrix-Clients. Laden Sie den Zwischenspeicher neu: Gehen Sie in den Element-Einstellungen in die Kategorie „Hilfe und Über“ und scrollen Sie ganz nach unten: „Zwischenspeicher löschen und neu laden“ sollte das Anzeigeproblem beheben.
***

#### Ist unser Server auf eurer Föderations-Blocklist? {#blocklist}
Aktuell befindet sich kein Server auf unserer Föderations-Blocklist. Dies kann nicht der Grund für etwaige Förderations-Probleme sein. Meldet euch aber gerne via [GWDG Support](https://gwdg.de/support)
***

#### Ich sehe in einem Raum von einer bestimmten Person keine Nachrichten {#blocked-user}
Ein häufig vorkommender Grund hierfür ist, dass Sie sich verklickt haben und die Person, von der Sie keine Nachrichten mehr sehen, obwohl Ihnen berichtet wird, dass dort etwas stehen müsste, von Ihnen blockiert wurde. Öffnen Sie hierzu Ihre Sicherheitseinstellungen und scrollen weit nach unten. Prüfen Sie, ob in der Kategorie „Blockierte Benutzer“ Einträge stehen, die dort nicht hingehören. Entfernen Sie diese gegebenenfalls.
***

# Login
#### Wie kann ich Matrix nutzen? / Ich finde keine Anleitung wie ich/andere Matrix nutzen können. {#how-to-login}
Anleitungen finden Sie für Element [für die Nutzung im Browser](/first-steps), auf [Android](/clients/android) und auf [iOS](/clients/ios) auf diesen Hilfeseiten.

Für andere Clients finden sich Anleitungen im Internet.
***

#### Ich habe mich an einem zweiten Gerät angemeldet und kann meine Nachrichten nicht lesen {#second-device-no-messages}
Verschlüsselte Nachrichten sind erst sichtbar, nachdem die neue Anmeldung verifiziert wurde. Dafür können Sie entweder
- Sicherheitsschlüssel oder Sicherheitspassphrase am neuen Gerät eingeben (diese wurden beim ersten Login festgelegt), oder
- Die zweite Anmeldung interaktiv verifizieren (man vergleicht Emoji zwischen der ersten und der zweiten Anmeldung).

Weitere Infos dazu gibt es [hier](/first-steps).
***

#### Ich habe Studien-/Forschungskollegen, die das auch nutzen wollen. Können die sich auch beim Academic Cloud Matrix anmelden? / Wie kann ich in Matrix mit Externen zusammenarbeiten? {#login-for-external-users}
Diese Matrix-Instanz ist auf Angehörige der Academic Cloud begrenzt. Allerdings ist es in Matrix egal, bei welchem Betreiber man angemeldet ist. Externe können also herausfinden, ob ihre Institution bereits Matrix betreibt, und
- falls ja, sich dort anmelden und sich wie gehabt in Chat-Räume oder Direktnachrichten einladen.
- falls nein, sich ein Konto bei einem beliebigen öffentlichen Matrix-Server anlegen (Listen gibt es z.B. [hier](https://joinmatrix.org/servers/)), und sich wie gehabt in Chat-Räume oder Direktnachrichten einladen.
***

# Nutzung des Dienstes
#### Wie teilt man Leuten eine Raumadresse mit? {#share-room}
Mit dem "https://matrix.to/..."-Link, den man unter dem i-Symbol für die Raumeigenschaften und einem weiteren Klick auf „Teile Raum“ erkennt.
***

#### Wie kann ich als administrierende Person viele Nachrichten auf einmal löschen? {#delete-multiple-messages}
Bitte melden Sie sich beim [GWDG Support](https://gwdg.de/support).
***

#### Manchmal sehe ich einen fett markierten Raum und klicke ihn an, habe aber doch nicht die Zeit, den Inhalt und etwaige Konsequenzen für mich sofort zu bearbeiten. Wie kann ich den Raum wieder als „ungelesen“ markieren? {#mark-room-as-unread}
In Element kann ein Raum mittels Rechtsklick 'Als Ungelesen markieren' wieder hervorgehoben werden. Über die Verfügbarkeit in anderen Programmen/ Apps, beachten Sie bitte deren Dokumentation.
***


# "Kann ich..?" (Features etc.)
#### Kann ich LaTeX schreiben? {#latex}
Ja! Es handelt sich allerdings um ein experimentelles Feature, Sie können es in den `Einstellungen` -> `Labor` -> `Nachrichtenübermittlung` einschalten und dann zwischen Dollar-Zeichen Latex schreiben: `$\LaTeX$`
***

#### Gibt es so etwas wie Threads (vgl. Rocket.Chat/ Slack) in Matrix? {#threads}
Ja, Matrix unterstützt die Nutzung von Threads. Diese sind allerdings noch recht neu und nicht in allen Clients optimal nutzbar. Die Unterstützung im empfohlenen Programm Element ist jedoch gut.
***

#### Ich habe 2 Accounts, kann ich Nachrichten vom einen zum anderen weiterleiten lassen? {#forward-account}
Nicht ohne weiteres, nein. Technisch ist das machbar, aber nur mit einigen Vorkenntnissen. Eine solche Konfiguration wird nicht aktiv durch uns unterstützt.
***

#### Kann ich in Matrix Videokonferenzen veranstalten? {#videoconf-in-matrix}
Zur Zeit werden nur 1:1-Anrufe (auch mit Video) unterstützt, in einigen Monaten werden evt. Gruppenanrufe mit prinzipiell unbegrenzter Teilnehmerzahl möglich sein. Wie viele Kamera-Bilder gleichzeitig genutzt werden können wird man dann testen können.

Eine Vorab-Testversion steht bereits zur Verfügung, Sie können diese in `Einstellungen` -> `Labor` einschalten.

Wir empfehlen die Nutzung des [GWDG BBB Dienstes](https://academiccloud.de/services/bigbluebutton/).
***

#### Kann man über Matrix Dateien versenden? / Was ist die maximale Dateigröße, die über Matrix verschickt werden kann? {#file-upload}
Im Matrix-Dienst ist im Moment das Hochladen von Dateien bis 250 Megabyte erlaubt. Für Nutzer bei anderen Betreibern, die ein geringeres Limit festgelegt haben, könnte es nicht möglich sein, größere Dateien herunterzuladen. In der Regel beträgt die Maximalgröße bei den meisten Betreibern 200 Megabyte.

Für Dateitransfers empfehlen wir generell eher [den Academic Cloud Service auf Basis von ownCloud](https://academiccloud.de/services/owncloud/) bzw. [GWDG FileSender](https://filesender.gwdg.de/).
***

#### Kann ich die/eine Matrix-App auf meinem Handy installieren, ohne Benachrichtigungen zu bekommen? {#app-without-notifications}
Ja, die meisten Apps erlauben es, Benachrichtigungen komplett auszuschalten. Dies ist in den Einstellungen der jeweiligen App möglich.

Auch können selektiv für besonders große/aktive/unwichtigere Chat-Räume die Benachrichtigungen ausgeschaltet werden, dies geht in der Regel indem man in der Raum-Liste lange auf den gewünschten Raum drückt und dann die Benachrichtigungs-Einstellungen am unteren oder oberen Bildschirmrand vornimmt (in Element erscheinen am unteren Bildschirmrand 4 mögliche Benachrichtigungs-Stufen).
***

#### Ist es möglich, benachrichtigt zu werden, wenn es neue Nachrichten in Matrix gibt, ohne eine App/Website zu öffnen? {#notifications-via-email}
Ja, es ist möglich, E-Mails zu bekommen wenn es im eigenen Matrix-Konto neue Nachrichten oder Raumeinladungen gibt. Weitere Infos gibt es [hier](/settings).
***

#### Kann ich mit Element mehrere Matrix-Accounts verwalten (Multi-Account-Client)? {#multiple-accounts-element}
Ein Element-Fenster kann zur Zeit nur einen Matrix-Account verwalten. Sie können allerdings zum Beispiel verschiedene Clients für die verschiedenen Accounts verwenden, unter anderem [SchildiChat](https://schildi.chat/), welcher große Ähnlichkeit mit Element hat. Zudem gibt es Clients, wie [FluffyChat](https://fluffychat.im/) oder [Fractal](https://matrix.org/ecosystem/clients/fractal/), welche mehrere Accounts in nur einer App (bzw. einem Browser-Tab) verwalten können.

Auch ist es möglich, mehrere Element-Fenster mit unterschiedlichen Matrix-Konten zu starten, auch im Autostart des Rechners. Dazu ist der Programmaufruf so abzuändern, dass ein spezifisches Profil geöffnet wird:
```
element-desktop --profile PROFILNAME
```
So lassen sich mehrere Starter im Autostart platzieren, die dann verschiedene Profilnamen haben, z.B. --profile acloud und --profile Privat. Beide geöffneten Fenster haben leider gleichaussehende Icons im Indicator-Applet.
***

#### Kann ich (Chat-)Bots oder Webhooks verwenden bzw. RSS-Feeds einbinden? {#hook}
Dies ist möglich. Laden Sie hierfür den Benutzer `@hookshot:gwdg.de` in ihren Kanal ein und geben Sie dem User das Power-Level 'Moderator'. Anschließend kann mit der Chatnachricht
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
***
