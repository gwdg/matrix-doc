---
title: "Erste Schritte"
date: 2020-08-02T21:26:25+02:00
chapter: true
draft: false
weight: 2
---

# Erste Schritte mit Matrix

## Matrix-Login mit TUB-Account

Mitgliedern und Angehörigen der TU Berlin (insbesondere auch Studierenden) wird durch Matrix ermöglicht, mittels ihres **TUB-Accounts** mit Angehörigen dieser und anderer Hochschulen und Universitäten sowie weiteren Matrix-Nutzenden (beispielsweise akademischen Partner:innen) per Chat sowie Audio-/Video-Telefonie zu kommunizieren.

Die Kommunikation erfolgt über einen sogenannten Client. Es steht eine [Vielzahl verschiedener Clients](https://matrix.org/clients/) zur Auswahl. Der bekannteste Client ist Element (früher Riot). Neben mobilen Versionen für Android und IOS bieten wir Element als Web-Anwendung unter [chat.tu-berlin.de](https://chat.tu-berlin.de) an. Element steht aber auch als Desktop-Anwendung zum Download bereit:

{{% button href="https://packages.riot.im/desktop/install/win32/x64/Element%20Setup.exe" icon="fas fa-download" %}}Windows{{% /button %}} {{% button href="https://packages.riot.im/desktop/install/macos/Element.dmg" icon="fas fa-download" %}}macOS{{% /button %}} {{% button href="/clients/install_linux" icon="fas fa-download" %}}Linux{{% /button %}}

{{% notice tip %}}
Wir empfehlen die Nutzung von Element als Web-Anwendung unter [chat.tu-berlin.de](https://chat.tu-berlin.de). Diese Version von Element ist auf unseren Matrix-Homeserver abgestimmt und wird regelmäßig aktualisiert.
{{% /notice %}}

Bei den mobilen Apps für Android und IOS sowie einer Desktop-Installation ist darauf zu achten, dass die Anmeldung mit dem TUB-Account auf unseren lokalen Homeserver erfolgt und kein neuer Account auf einem anderen Homeserver erstellt wird. Dazu muss man im Client die URL des lokalen Homeservers eintragen. Hier am Beispiel von Element-Desktop:

![Markierter Anmeldebutton im Element Matrixclient](/images/01_Login_de.png)

Um sich auf dem Homeserver der TU Berlin anzumelden, klickt man zunächst auf **Anmelden** und anschließend auf **Bearbeiten**.

![Anmeldeseite mit Fokus auf dem Homeserver ändern Button](/images/02_Change-Homeserver_de.png)

Nun kann man manuell *matrix.tu-berlin.de* als Homeserver angeben.

![Eingabefeld zum Ändern des Homeservers mit der Eingabe matrix.tu-berlin.de](/images/03_Set-Homeserver_de.png)

Anschließend müssen Benutzername und Passwort des TUB-Accounts angegeben werden. In dem Dropdown-Menü „Anmelden mit:“ sollte „Benutzername“ ausgewählt bleiben. Als Nutzername muss der TUB-Login **vollständig in Kleinbuchstaben** verwendet werden (keine E-Mail-Adresse). Es folgt nach dem Erstlogin auch keine Bestätigungsmail.

![Loginfenster mit Aufforderung TUB-Login und Passwort einzugeben](/images/04_Username_de.png)

Analog zu E-Mail-Adressen ergibt sich eine Matrix-Adresse, über die man über einen Client (z.B. Element) zur Kommunikation eingeladen werden kann:

<p style="text-align: center; font-style: italic;">@&lt;tu_login&gt;:matrix.tu-berlin.de</p>

Unter Umständen werden Sie nach der ersten Anmeldung dazu aufgefordert die Schlüsselsicherung einzurichten oder andere wichtige Einstellungen vorzunehmen. Wir empfehlen sich die Zeit zu nehmen und den Aufforderungen zu folgen. [Hier finden Sie Hinweise zu den Einstellungen.]({{< relref "settings/_index.md" >}})

![Aufforderung den Sicherheitsschlüssel zu generieren oder eine Sicherheitsphrase einzugeben](/images/11_Setup-Key_de.png)

## Matrix-Login ohne TUB-Account

Eine Registrierung von Accounts (wie vielleicht von anderen Matrix-Servern bekannt) ist hier an der TU Berlin nicht möglich, da den Dienst ausschließlich Personen mit TUB-Login nutzen können. Es ist jedoch möglich mit Nutzern anderer Matrix-Homeserver von verschiedenen wissenschaftlichen und zivilgesellschaftlichen Institutionen zu komminizieren. Dieses Feature nennt sich Förderation (das Prinzip ist ähnlich zu dem E-Mail System: E-Mails können beispielsweise von den Servern der TU Berlin an die Sever TU Dresden geschickt werden). Auf öffentlichen Homeservern, wie zum Beispiel dem von [matrix.org](https://app.element.io/), kann sich jede Person einen Account anlegen.

Folgende deutsche Hoschulen verfügen über einen eigenen Homeserver:

* [TU Freiberg](https://matrix.tu-freiberg.de/) inkl. [Doku](https://tu-freiberg.de/en/urz/dienste/chat)

* [TU Chemnitz](https://matrix.tu-chemnitz.de) inkl. [Doku](https://www.tu-chemnitz.de/urz/groupware/chat/doku/)

* [Hochschule Darmstadt](https://chat.fbi.h-da.de) inkl. [Doku](https://its.h-da.io/element-docs/)

* [Hochschule Zittau-Görlitz](https://matrix.hszg.de) inkl. [Doku](https://zfe.hszg.de/das-zfe/aktuelle-entwicklungen/matrix)

* [HMT Leipzig](https://chat.hmt-leipzig.de)

* [Uni Kiel](https://riot.fs-infmath.uni-kiel.de) inkl. [Doku](https://www.fs-infmath.uni-kiel.de/wiki/Technische_Dienste)

* [Uni Hamburg](http://uni-hamburg.de/)

* [Uni Bremen](https://element.stugen.de/#/welcome)

* [TU Dresden](https://matrix.tu-dresden.de/) inkl. [Doku](https://doc.matrix.tu-dresden.de/)

* [Humboldt Uni Berlin](https://element.hu-berlin.de/) inkl. [Doku](https://www.digitale-lehre.hu-berlin.de/de/lehr-und-lernlandschaft/element)

* [TU München](https://matrix.tum.de) inkl. [Doku](https://wiki.in.tum.de/Informatik/Helpdesk/RIOT)

* [Uni Hannover](https://matrix.uni-hannover.de) inkl. [Doku](https://www.luis.uni-hannover.de/de/services/kommunikation/matrix-messenger/)

* [Uni Osnabrück](https://chat.virtuos.uni-osnabrueck.de/#/welcome) inkl. [Doku](https://www.rz.uni-osnabrueck.de/homeoffice/riot.html)

* [Uni Bielefeld](https://uni-bielefeld.de/teamchat2)

* [Bauhaus-Universität Weimar](https://matrix.bau-ha.us) inkl. [Doku](https://m18.uni-weimar.de/stuko/referate/digitale-infrastruktur)

* [RWTH Aachen](https://riot.comsys.rwth-aachen.de/)

* [Ruhr Universität Bochum](https://riot.rub.de/) inkl. [Doku](https://www.it-services.ruhr-uni-bochum.de/services/issi/element.html.de)

* [Uni Bonn](https://element.matrix.informatik.uni-bonn.de/)

* [Uni Heidelberg](https://matrix-im.uni-heidelberg.de/) inkl. [Doku](https://www.urz.uni-heidelberg.de/en/heichat)

* [Karlsruher Institut für Technologie (KIT)](https://matrix.kit.edu/)

* [Uni Augsburg](https://element.physik.uni-augsburg.de/#/welcome) inkl. [Doku](https://www.uni-augsburg.de/de/fakultaet/mntf/physik/facilities/itservices/elequick/)

* [Uni Stuttgart](https://chat.stuvus.de/) inkl. [Doku](https://wiki.stuvus.uni-stuttgart.de/display/ITKB/Matrix+Messenger)

* [Hochschule Bremerhaven](https://matrix.hs-bremerhaven.de/)

* [TU Darmstadt](https://element.matrix.tu-darmstadt.de)

* [Philipps-Universität Marburg](https://matrix.uni-marburg.de/)

* [TU Braunschweig](https://chat.tu-bs.de/)

* [Hochschule Furtwangen](https://matrix.hs-furtwangen.de/) inkl. [Doku](https://howto.hs-furtwangen.de/hfu-chat/)

* [Friedrich-Alexander-Universität Erlangen-Nürnberg](https://chat.fau.de/) inkl. [Doku](https://www.rrze.fau.de/serverdienste/matrix/)

* [Friedrich-Schiller-Universität Jena](https://chat.uni-jena.de/) inkl. [Doku](https://wiki.uni-jena.de/display/URZ010SD/Chatten+mit+Matrix)


Explizit für Studierende:

* [StudiChat](https://chat.studichat.de/#/welcome) (für alle)

* [Fachschaften](https://matrix.fachschaften.org/) (für Fachschaften)

Weitere europäische Hochschulen:

* [ETH Zürich](https://element.phys.ethz.ch/) inkl. [Doku](https://readme.phys.ethz.ch/chat/)

* [Universität Innsbruck](https://chat.uibk.ac.at/) inkl. [Doku](https://www.uibk.ac.at/zid/anleitungen/chat/)

* [University for Business and Technology, Kosovo](https://ubt-uni.net/)

* [Karl-Franzens-Universität Graz](https://chat.uni-graz.at/)

Kartendarstellung der Hochschulen und Universitäten mit einem Matrix-Dienst:

<object data="/images/federation_map.svg" type="image/svg+xml" style="width: 600px; max-width: 100%"></object>

Für die zivilgesellschaftliche Nutzung des Protokolls Matrix gibt es hier eine Liste an öffentlichen Homeservern, die auch von Kolleg:innen genutzt werden können, falls ihre Institution noch keinen Matrix-Server anbietet:

[https://austinhuang.me/matrix-homeservers.html](https://austinhuang.me/matrix-homeservers.html)

[https://www.hello-matrix.net/public_servers.php](https://www.hello-matrix.net/public_servers.php)

[https://publiclist.anchel.nl/](https://publiclist.anchel.nl/)

[https://fediverse.blog/~/FossMessenger/matrix-server](https://fediverse.blog/~/FossMessenger/matrix-server)

<!--
## Datenschutzerklärung

Datenschutzerklärung: [Link](https://matrix.tu-berlin.de/_matrix/consent)

## Impressum

Impressum: [Link]({{< relref "imprint/_index.md" >}})
-->
