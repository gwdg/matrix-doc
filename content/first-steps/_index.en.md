---
title: "First steps"
date: 2020-08-02T21:26:25+02:00
chapter: false
weight: 2
---

## Matrix Login with Academic ID ##

All Academic Cloud users are enabled to chat with each other as well as matrix users at different universities and research institutes using  the GWDG matrix service in compliance with the relevant legal and regulatory provisions on data protection and IT security. 

{{% notice tip %}}
We recommend using the Element desktop client, because this avoids most problems users have with Matrix, e.g. end-to-end encryption.
{{% /notice %}}

Downloads for: {{% button href="https://packages.riot.im/desktop/install/win32/x64/Element%20Setup.exe" icon="fas fa-download" %}}Windows{{% /button %}} {{% button href="https://packages.riot.im/desktop/install/macos/Element.dmg" icon="fas fa-download" %}}macOS{{% /button %}} {{% button href="/clients/install_linux" icon="fas fa-download" %}}Linux{{% /button %}}

After a desktop installation, make sure to use the existing account with the Academic ID and not to create a new account on another server. Here the example of Element:

![Selected login button in the element matrix client](/images/01_Login_en.png)

This is done by clicking on **Change**. Then you will not accidentally end up on the wrong server...

![Change login page with focus on the homeserver button](/images/02_Change-Homeserver_en.png)

Now you can manually specify the home server:

| Institution | Home Server |
|---|---|
| Max-Planck-Gesellschaft | matrixchat.mpg.de |
| Georg-August-Universität Göttingen | chat.uni-goettingen.de |
| Universitätsmedizin Göttingen  | chat.umg.eu |
| GWDG | matrix.gwdg.de |
| Academic Cloud | chat.academiccloud.de |

![Input field to change the home server with the input matrix.tu-dresden.de](/images/03_Set-Homeserver_en.png)

Afterwards you can login via the Academic Cloud:

![Academic Cloud SSO Login](/images/03_Browser_Academic_Cloud_SSO_de.png)

Analogous to e-mail addresses, this results in matrix addresses with the following structure:

@username:academiccloud.de

## Convenient use of end-to-end encryption (E2EE)

Matrix not only encrypts transports to and from the home server (in the data center of the GWDG) but also allows the use of end-to-end encryption (E2EE). For this, cryptographic keys have to be exchanged between all devices that want to write end-to-end encrypted. This technical necessity sounds and is complicated, but in the meantime it has become very convenient for the users. The many cryptographic keys created by the client are stored on the respective device. If this is a tab in a browser, for example, there is a risk that this tab will be closed unintentionally. Then all encrypted contents are no longer readable. To prevent this from happening, a key protection is offered on the home server of the Academic Cloud, on which (protected with a security phrase or security key that can be calculated from it) all cryptographic keys are stored encrypted. 
   
{{% notice info %}}
It is highly recommended to use this key backup (with a secure security phrase which is NOT your Academic Cloud password)!
{{% /notice %}}
   
![Prompt to generate the security key or enter a security phrase](/images/11_Setup-Key_en.png)
![Prompt to enter a password for the key backup](/images/12_Enter-Key_en.png)
Alternatively, instead of the security phrase, you can also have a security key generated that serves the same purpose as the security phrase. Furthermore, the security key is generated in addition to the security phrase and should be kept safe and retrievable as an emergency key (e.g. save it as .txt file AND print it out) 
![Display of the security key to write or save away](/images/13_Present-Key_en.png) 

[Other important settings]({{% relref "settings/_index.en.md" %}}) may improve your Matrix experience!


## Requests to setup the key backup

![Screenshot of the prompt to enter a security phrase](/images/01_Restore-Session_en.png)

If you skipped the request to setup the key backup, the next screen would look like this:

![Confirmation of skipping the input of a security phrase](/images/03_Cancel-Restore_en.png)

Key protection is highly recommended for worry-free end-to-end encryption. For this reason, a smaller tooltip will prompt you to set up the encryption even after you skip further:
   
![Chat view showing a tooltip to set up encryption. Marking the confirm field](/images/04_Notification_en.png)

If you omit this here as well, you will get a last warning if you log off consciously. If no key backup is set up at the latest, encrypted calls that may have already taken place cannot be accessed later. If the tab is closed, this also corresponds to a logout.
   
![Query if messages should be encrypted](/images/05_Logout-Notify_en.png)

Avoid this situation by setting up a key backup!

## Matrix Login without Academic ID
It is not possible to register a matrix account directly. However, matrix is available for guests accounts, which can be created on [Academic Cloud](https://academiccloud.de).
