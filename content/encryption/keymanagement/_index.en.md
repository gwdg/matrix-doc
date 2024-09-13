---
title: "Key Management"
date: 2024-08-08T16:49:12+02:00
chapter: false
draft: false
weight: 2
---

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
