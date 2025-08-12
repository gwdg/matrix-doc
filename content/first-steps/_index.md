---
title: "Erste Schritte"
date: 2024-08-08T16:49:12+02:00
chapter: false
draft: false
weight: 2
---

## Matrix-Login mit Academic ID ##

Allen Nutzenden der Academic Cloud wird unter Einhaltung der einschlägigen gesetzlichen und rechtlichen Bestimmungen zum Datenschutz und zur IT-Sicherheit ermöglicht, mittels ihrer **Academic ID** mit Angehörigen ihrer und anderer Hochschulen, Universitäten und Institute sowie weiteren Matrix-Nutzenden (bspw. akademischen Partner*innen) per Chat zu kommunizieren.  
Der Dienst wird über einen Client genutzt, es stehen eine [Vielzahl verschiedener Programme]({{% relref "clients/_index.md" %}}) zur Auswahl. Der bekannteste Client ist Element (früher Riot), neben der Desktop-Anwendung und mobilen Versionen für Android und iOS für Ihre Geräte betreibt die GWDG Element auch als Web-Anwendung. 

Element steht als Desktop-Anwendung zum Download bereit:

{{% button href="https://packages.riot.im/desktop/install/win32/x64/Element%20Setup.exe" icon="fas fa-download" %}}Windows{{% /button %}} {{% button href="https://packages.riot.im/desktop/install/macos/Element.dmg" icon="fas fa-download" %}}macOS{{% /button %}} {{% button href="/clients/install_linux" icon="fas fa-download" %}}Linux{{% /button %}}

{{% notice tip %}}
Wir empfehlen die Nutzung von Element als Desktop-Anwendung bzw. mobilen Client oder die von der GWDG bereitgestellte Web-Anwendung.
{{% /notice %}}

Die folgenden Screenshots zeigen beispielhaft die Nutzung von [chat.academiccloud.de](https://chat.academiccloud.de) im Browser, bei den anderen Instanzen können die Screenshots in Details abweichen.

| Institution | Server |
|---|---|
| Max-Planck-Gesellschaft | [matrixchat.mpg.de](https://matrixchat.mpg.de) |
| Georg-August-Universität Göttingen | [chat.uni-goettingen.de](https://chat.uni-goettingen.de) |
| Universitätsmedizin Göttingen  | [chat.umg.eu](https://chat.umg.eu) |
| GWDG | [matrix.gwdg.de](https://matrix.gwdg.de) |
| Academic Cloud | [chat.academiccloud.de](https://chat.academiccloud.de) |
| Universität Kassel | [matrix.uni-kassel.de](https://matrix.uni-kassel.de) |

Den [Start mit der Desktop-Anwendung beschreiben wir hier]({{% relref "first-steps/_index.md/#zugriff-vom-desktop-oder-mit-mobilen-clients" %}}).

![Startseite des Element Webclient mit Anmeldebutton](/images/01_Browser_Welcome_de.png)

Falls Sie bereits eine Academic ID haben, ist keine weitere Registrierung nötig, der Dienst kann nach dem Login sofort genutzt werden.

![Loginfenster mit einem Knopf welcher zum Academic Cloud SSO Login weiterleitet](/images/02_Browser_Login_de.png)

Ihr Heimserver ist vorkonfiguriert, klicken Sie auf "Fortfahren", Sie werden zum Academic Cloud SSO geleitet. Falls Sie noch nicht angemeldet sind, loggen Sie sich mit Ihrer Academic ID und ggf. Ihrem zweiten Faktor ein.

![Academic Cloud SSO Login](/images/03_Browser_Academic_Cloud_SSO_de.png)

Ihre Account-Daten (Anzeigename & E-Mail-Adresse) werden aus der Benutzerverwaltung übertragen, eine Änderung ist an dieser Stelle nicht möglich.

![Übertragung der Account-Daten](/images/04_Browser_Data_Import_de.png)

Bestätigen Sie, dass der Dienst (in diesem Fall chat.academiccloud.de) Ihre Daten verarbeiten darf.

![Zugriff bestätigen](/images/05_Browser_Allow_Access_de.png)

Der Browser muss lokale Daten auf Ihrem PC speichern, erlauben Sie diesen Zugriff.

![Datenzugriff im Browser bestätigen](/images/06_Browser_Allow_Data_Storage_de.png)

Unter Umständen werden Sie nach der ersten Anmeldung dazu aufgefordert die Schlüsselsicherung einzurichten oder andere wichtige Einstellungen vorzunehmen. Wir empfehlen, sich die Zeit zu nehmen und den Anweisungen zu folgen. [Hier finden Sie Hinweise zu den Einstellungen.]({{% relref "settings/_index.md" %}})

{{% notice tip %}}
Wir raten dringend dazu, die [Schlüsselsicherung]({{% relref "encryption/keymanagement/_index.md" %}}) einzurichten. Bei Verlust aller Schlüsselkopien sind verschlüsselte Chats sonst nicht mehr lesbar.
{{% /notice %}}

## Zugriff vom Desktop oder mit mobilen Clients ##

Bei den mobilen Apps für Android und iOS sowie einer Desktop-Installation müssen Sie darauf achten, dass die Anmeldung auf Ihrem Homeserver erfolgt und Sie sich kein neuen Account auf einem anderen Homeserver erstellen (das _können_ Sie natürlich tun, aber mit dem neuen Account haben Sie dann keinen Zugriff auf Ihre Daten).  
Dazu müssen Sie im Client die URL des lokalen Homeservers eintragen.

Hier am Beispiel von Element-Desktop:

![Markierter Anmeldebutton im Element Matrixclient](/images/01_Desktop_Welcome_de.png)

Um zu Ihrem Homeserver zu wechseln, klicken Sie zunächst auf **Anmelden** und anschließend auf **Bearbeiten**.

![Anmeldeseite mit Fokus auf dem Homeserver ändern Button](/images/02_Desktop_Choose_Homeserver_de.png)

Nun können Sie Ihren Homeserver angeben:

| Institution | Server |
|---|---|
| Max-Planck-Gesellschaft | matrixchat.mpg.de |
| Georg-August-Universität Göttingen | chat.uni-goettingen.de |
| Universitätsmedizin Göttingen  | chat.umg.eu |
| GWDG | matrix.gwdg.de |
| Academic Cloud | chat.academiccloud.de |

![Eingabefeld zum Ändern des Homeservers mit der Eingabe matrix.tu-berlin.de](/images/03_Desktop_Set_Homeserver_de.png)

Bestätigen Sie Ihre Eingabe und Sie werden zum Academic Cloud SSO geleitet, um sich anzumelden und die Übertragung und Verabeitung Ihrer Daten durch die Anwendung zu bestätigen.  
Das Program Elements-Desktop taucht dabei als `element://vector/webapp/` auf.

![Weiterleitung zum SSO](/images/04_Desktop_SSO_de.png)

Ab hier funktioniert der Ablauf in der Desktop-Anwendung genau wie bei der Webseite. Unter Umständen werden Sie nach der ersten Anmeldung dazu aufgefordert, die Schlüsselsicherung einzurichten oder andere wichtige Einstellungen vorzunehmen. Wir empfehlen sich die Zeit zu nehmen und den Anweisungen zu folgen. [Hier finden Sie Hinweise zu den Einstellungen.]({{% relref "settings/_index.md" %}})

{{% notice tip %}}
Wir raten dringend dazu, die [Schlüsselsicherung]({{% relref "encryption/keymanagement/_index.md" %}}) einzurichten. Bei Verlust aller Schlüsselkopien sind verschlüsselte Chats sonst nicht mehr lesbar.
{{% /notice %}}

## Neue Geräte hinzufügen ##

Wenn Sie sich auf weiteren Geräten anmelden wollen, müssen Sie diese für den Zugriff auf Ihren Account freischalten. Dazu stehen zwei Möglichkeiten zur Verfügung:  
Sie können das neue Gerät entweder mit einem bereits angemeldeten Gerät oder mit Ihrer Sicherheitsphrase bzw. Ihrem Sicherheitsschlüssel verifizieren.
Bei “Mit anderem Gerät verifizieren” werden Ihnen auf beiden Geräten eine Reihe von Emoji angezeigt und Sie werden aufgefordert zu bestätigen, dass sie auf beiden Geräten übereinstimmen. Die Android- und iOS-Clients bieten dazu noch einen QR-Code zur Verifizierung an.

![ein neues Geraet verifizieren](/images/13_Browser_Geraet_verfizieren.png)

## Matrix-Login ohne Academic ID ##

Eine Registrierung von Accounts (wie vielleicht von anderen Matrix-Servern bekannt) ist an den von der GWDG betriebenen Matrix-Instanzen nicht möglich. Für den Zugang zum Dienst ist ein Login mit Academic ID notwendig. Für Nutzer*innen von Academic Cloud Gast-Accounts ist der Matrix-Homeserver (analog zur bisherigen Praxis bei Rocketchat) freigeschaltet.  
Es ist auch möglich mit Nutzern anderer Matrix-Homeserver von verschiedenen wissenschaftlichen und zivilgesellschaftlichen Institutionen zu kommunizieren. Dieses Feature nennt sich Förderation. Das Prinzip ist ähnlich zu E-Mail: E-Mails können beispielsweise von den Servern der GWDG an die Hochschule Hannover geschickt werden.  
Auf öffentlichen Homeservern, wie zum Beispiel dem von [matrix.org](https://app.element.io/), kann sich jede Person einen Account anlegen.
