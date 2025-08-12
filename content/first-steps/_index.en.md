---
title: "First steps"
date: 2020-08-02T21:26:25+02:00
chapter: false
weight: 2
---

## Matrix Login with Academic ID

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

| Institution | Server |
|---|---|
| Institution | Home Server |
|---|---|
| Max-Planck-Gesellschaft | https://matrixchat.mpg.de |
| Georg-August-Universität Göttingen | https://chat.uni-goettingen.de |
| Universitätsmedizin Göttingen  | https://chat.umg.eu |
| GWDG | https://matrix.gwdg.de |
| Academic Cloud | https://chat.academiccloud.de |
| Universität Kassel | https://matrix.uni-kassel.de |

![Input field to change the home server with the input matrix.tu-dresden.de](/images/03_Set-Homeserver_en.png)

Afterwards you can login via the Academic Cloud:

![Academic Cloud SSO Login](/images/03_Browser_Academic_Cloud_SSO_de.png)

Analogous to e-mail addresses, this results in matrix addresses with the following structure:

@username:academiccloud.de

{{% notice warning %}}
We highly recommend to [set up your key backup]({{% relref "encryption/keymanagement/_index.en.md" %}}) as the next step!
{{% /notice %}}

## Matrix Login without Academic ID
It is not possible to register a matrix account directly. However, matrix is available for guests accounts, which can be created on [Academic Cloud](https://academiccloud.de).
