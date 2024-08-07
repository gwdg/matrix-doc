---
title: "Element Web (Browser)"
date: 2020-07-15T16:46:07+02:00
draft: false
chapter: true
weight: 5
---

# Element Web

Starten Sie auf [chat.academiccloud.de](https://chat.academiccloud.de).

![Startseite von Element Webclient mit Anmeldebutton](/images/01_Welcome_de.png)

Hierzu ist keine Konfiguration oder Registrierung nötig, der Dienst kann sofort durch Klick auf „Anmelden“ auf der Startseite [chat.academiccloud.de](https://chat.academiccloud.de) genutzt werden.

![Loginfenster mit Aufforderung ZIH Login und Passwort einzugeben](/images/02_Login1_de.png)

Anschließend müssen Benutzername und Passwort des TUB-Accounts angegeben werden. In dem Dropdown-Menü „Anmelden mit:“ sollte „Benutzername“ ausgewählt bleiben. Als Nutzername muss der TUB-Login **vollständig in Kleinbuchstaben** verwendet werden (keine E-Mail-Adresse). Es folgt nach dem Erstlogin auch keine Bestätigungsmail.

{{% notice warning %}}
Sollten Sie statt mit der oben genannten Website (Element-Web-App der Academic Cloud) sofort mit einem [Matrix Client]({{< relref "../clients" >}}) starten wollen, ist es wichtig den Heimserver vom zumeist standardmäßig eingestellten matrix.org auf academiccloud.de zu ändern siehe [Erste Schritte]({{< relref "../first-steps" >}}).
{{% /notice %}}

Der einfachste Weg ist das direkte Öffnen der Element-Web-Anwendung in einem modernen Browser (z.B. [Mozilla Firefox](https://www.mozilla.org/de/firefox/)) unter der Adresse [chat.academiccloud.de](https://chat.academiccloud.de).

## Browsereinstellungen

### Browserwahl

Empfehlenswert sind die Browser [Firefox](https://www.mozilla.org/de/firefox/new/), [Chromium](https://www.chromium.org/getting-involved/download-chromium), neuere Versionen von Microsoft Edge (basierend auf Chromium). Ältere oder ungeeignete Browser zeigen unter Umständen nur eine weiße Seite an.

### NoScript

Sollten Sie Browser-Plugins (z.B. Skript-Blocker) nutzen, um sich vor [Tracking](https://tu-dresden.de/tu-dresden/newsportal/news/datenschutz-beim-website-tracking) und Schadsoftware im Browser zu schützen, beispielsweise mit dem Addon [NoScript](https://addons.mozilla.org/de/firefox/addon/noscript/). Hier sind folgende Einstellungen durchzuführen (für den Integrationsmanager, z.B. Jitsi/Etherpad)

![Einstellungen des Browserplugins NoScript mit tu-dresden.de und vector.im als vertrauenswürdige Skriptquellen ausgewählt](/images/10_Sicherheit2_de.png)

### Cookies

Erlauben Sie auch dauerhaft Cookies von

- academiccloud.de
- vector.im (für den Integrationsmanager)

So ist u.a. sichergestellt, dass die Sitzung stabil bestehen bleibt und damit die Schlüssel der Ende-zu-Ende-Verschlüsselung nicht verlorengehen.
