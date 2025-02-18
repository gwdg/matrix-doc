---
linktitle: "FAQ"
title: "Frequently asked questions"
date: 2020-08-02T21:26:25+02:00
draft: false
weight: 200
---
This is a compilation of frequently asked questions and their answers. In some cases, the answers have not yet been formulated. In these cases, please ask in the [#helpdesk:kit.edu](https://matrix.to/#/#helpdesk:kit.edu) room.

- [Message cannot be decrypted](#unable-to-decrypt)
- [I do not have a recovery key](#no-recovery-key)
- [How do I change the security phrase for my key backup?](#change-securityphrase)
- [How can I reset the key backup if I have lost my security phrase AND my security key?](#reset-securityphrase)
- [What should I do if video or audio in a video conference does not work on a Mac or MacBook?](#apple-no-video)
- [I cannot invite a fellow student or researcher](#unable-to-invite)
- [The connection to the server has been lost](#no-connection)
- [My client says „missing translation: ...“ everywhere](#missing-translations)
- [Is our server on your federation blocklist?](#blocklist)
- [I do not see any messages from a certain person in a room](#blocked-user)
- [How can I use matrix? / I can't find instructions on how I or others can use matrix.](#how-to-login)
- [I have logged on to a second device and cannot read my messages](#second-device-no-messages)
- [I have study/research colleagues who also want to use this. Can they also register with this matrix? / How can I collaborate with externals in matrix?](#login-for-external-users)
- [How do you tell people a room address?](#share-room)
- [How can I as an admin delete many messages at once?](#delete-multiple-messages)
- [Sometimes I see a bold marked room and click on it, but yet I don't have the time to immediately edit the content and any consequences for me. How can I mark the room as "unread" again?](#mark-room-as-unread)
- [Can I write LaTeX?](#latex)
- [Is there such a thing as threads (as in Mattermost/Slack) in matrix?](#threads)
- [I have multiple accounts, can I have messages forwarded from one to the other?](#forward-account)
- [Can I hold video conferences in matrix?](#videoconf-in-matrix)
- [Is it possible to send files via matrix? / What is the maximum file size that can be sent via matrix?](#file-upload)
- [Can I install a matrix app on my phone without getting notifications?](#app-without-notifications)
- [Is it possible to be notified when there are new messages in matrix without opening an app/website?](#notifications-via-email)
- [Can I manage multiple matrix accounts with Element (multi-account client)?](#multiple-accounts-element)
- [How can I operate a (chat)bot in Matrix?](#hook)

***
# Troubleshooting

#### Message cannot be decrypted {#unable-to-decrypt}
- **Does this occur with all messages in a room (or all messages in all private rooms)?**
  The login where the messages are not visible has not been verified. Please either
    - Enter security key or security passphrase (these were set at your first login), or
    - Verify this login interactively (you compare emoji between the first and the second login). More info about this can be found [here](/en/first-steps).
    - Check if the setting "Encrypt to verified sessions only from this session" is set. The setting can be set for each login/device or for each room. The setting issues, that unverified counterparts cannot read messages sent from this device / in this room. Security-conscious users without Matrix experience may activate the setting without understanding its implications. The setting makes sense when writing with personally known **and verified** counterparts and can increase security there. However, if you want to exchange messages with not yet verified strangers (especially in groups), you should set this setting with caution and only per room (e.g. for rooms with sensitive content). Security-conscious users should trust and pay more attention to the display of green/red shields next to names and red schields next to messages.
- **Does this only occur with messages in a certain time period?**
  Most likely, no device was logged in with your account during that time period. To use matrix safely, it is *not* necessary to log out of sessions (e.g. before closing the browser), so it is recommended to just stay logged in on devices you want to use again and close the website/app directly if desired. This way, messages can be correctly encrypted and delivered even when no device is switched on.
  If you were always logged in with at least one device, your browser settings (if you use Element in the browser) could also cause the problem. Make sure that the browser does not delete local data, cookies or similar on its own.
- **Does this occur sporadically / only once?**
  You can first check if there are logins for your account that are not verified (this can usually be found in security settings of the respective app or website), and ask the sender of the message to do the same. Sometimes this error is unrecoverable, in which case it's best to ask the sender to resend the message.
***

#### I do not have a recovery key {#no-recovery-key}
Please check whether you have set up the secure key backup. See [Key Backup](/en/settings/#key-backup).
***

#### How do I change the security phrase for my key backup? {#change-securityphrase}
- For all matrix sessions except one, which is still accessible, export the room keys `Settings` -> `Security & Privacy` -> `Encryption`. Finally, log out by clicking on the user name in the upper left corner and log out. If you are asked whether you want the encrypted messages, click on 'I don't want my encrypted messages', because these keys have already been exported.
- Under `Settings`-> `Security & Privacy` -> `Secure Backup` first click the button `Delete Backup`, then the button `Reset`, possibly a deletion of the cache under `Settings`-> `Help & About` is necessary, possibly also a logout and a new logon with a subsequent new attempt. If all this does not work, continue in the next point. The action was successful, if only the green Setup button is displayed.
- For all previously exported key backups, perform the manual import procedure.
- Set up a new key backup. See [Key Backup](/en/settings/#key-backup).
***

#### How can I reset the key backup if I have lost my security phrase AND my security key? {#reset-securityphrase}
Please note: You can use the reset to obtain a ‘verified’ session again. As soon as you have a verified session, you can also log in to other devices and verify them via the first session, but we strongly recommend using the Element Client as the ‘main session’. Depending on your operating system there is a program for it, for this see the [first steps](/first-steps/index.html).

Please do the following:
   1. Export the room keys in a matrix session (=client/devices/browser) where you can still read the previous encrypted messages. To do this, go to `Settings`-> `Security` -> `Encryption` and click on Export E2E room keys. If there is no longer access to a matrix session in which previous encrypted messages are readable, or if old messages do not necessarily need to be preserved, this step may be skipped.
  2. Depending on the instance, see the following table, log in to the corresponding auth-instance and log out of the active sessions via ‘My account’ -> ‘Devices’. You should not log out of the ‘active now’ browser session, this refers to the session on the auth-instance, which is still required below.

     | Institution | auth-instance |
     | ----------- | ------------ |
     | Academic Cloud | [https://auth.chat.academiccloud.de](https://auth.chat.academiccloud.de) |
     | Georg-August-Universität Göttingen | [https://auth.chat.uni-goettingen.de](https://auth.chat.uni-goettingen.de) |
     | GWDG | [https://auth.matrix.gwdg.de](https://auth.matrix.gwdg.de) |
     | Max-Planck-Gesellschaft | [https://auth.matrixchat.mpg.de](https://auth.matrixchat.mpg.de) |
     | Universitätsmedizin Göttingen  | [https://auth.chat.umg.eu](https://auth.chat.umg.eu) |

  3. In the same browser window, i.e. on the auth-instance, switch to the ‘Settings’ tab, open the ‘End-to-end encryption’ item and click the red ‘Reset identity’ button.
  4. Switch back to the client (e.g. the element-client, we strongly recommend not to use the browser) and log out if you were not logged out automatically. Log back in again. If you are asked to put your security key or security phrase, select the option to reset it (should appear below the text field).
  5. After login you are asked to create a new security key phrase or password. Select one and create it and *SAVE IT SECURELY*, e.g. printing it or using a password-manager like KeePassXC or similar. To do this you may also follow [these steps](/settings/index.html).

After the new login you session should be verified. If necessary you may also log into other clients, e.g. a smartphone, for verification you need to verify the login in the element client-session, so to speak the ‘main session’. Exchange of all necessary keys will then happen automatically in the background.

***

#### What should I do if video or audio in a video conference does not work on a Mac or MacBook? {#apple-no-video}
Often Element does not have the rights to access the webcam and microphone. These can be assigned in the system settings under Security and Privacy.
***

#### I cannot invite a fellow student or researcher {#unable-to-invite}
- First check the spelling (was the acronym or name really entered correctly?).
- It is not possible to invite or search for users with their e-mail address. It is best to either search for the acronym (if known), or "on the off chance" search for the person's first and/or last name (this only works if the person has chosen them as the display name).
- Users can only be invited if they have registered at least once. If the acronym / matrix ID can not be found, this user has never logged into matrix.
***

#### The connection to the server has been lost {#no-connection}
1. Does your device have access to the Internet? Make sure that it is not a missing mobile connection, unplugged internet cable, or similar.
2. For maintenance of the system, the matrix server is sometimes restarted briefly, in this case the service is available again after a few minutes.
***

#### My client says „missing translation: ...“ everywhere {#missing-translations}
This phenomenon is often related to unfinished updates of the matrix client. Reload the cache: Go to the "Help and About" category in the Element settings and scroll all the way down: "Clear cache and reload" should fix the display problem.
***

#### Is our server on your federation blocklist? {#blocklist}
Currently there is no server on our Federation blocklist. This cannot be the reason for any Federation problems.
***

#### I do not see any messages from a certain person in a room {#blocked-user}
A common reason for this is that you have misclicked and the person you no longer see messages from, even though you are told there should be something there, has been blocked by you. To do this, open your security settings and scroll way down. Check if there are entries in the "Blocked users" category that don't belong there. Remove them if necessary.
***

# Login
#### How can I use matrix? / I can't find instructions on how I or others can use matrix. {#how-to-login}
For instructions, see these help pages for Element [for use in the browser](/en/first-steps"), on [Android](/en/clients/android), and on [iOS](/en/clients/ios).

For other clients, instructions can be found on the internet as well.
***

#### I have logged on to a second device and cannot read my messages {#second-device-no-messages}
Encrypted messages are only visible after the new login has been verified. For this you can either
- Enter security key or security passphrase on the new device (these were set during the first login), or
- Verify the second login interactively (you compare emoji between the first and second login).

More info about this can be found [here](/en/first-steps).
***

#### I have study/research colleagues who also want to use this. Can they also register with this matrix? / How can I collaborate with externals in matrix? {#login-for-external-users}
This matrix service is limited to members of the Academic Cloud. However, in matrix it does not matter with which operator one is registered. So external users can find out if their institution is already running matrix and
- if yes, register there and be invited to chat rooms or direct messages as usual.
- if not, create an account at any public matrix server (lists are available e.g. [here](https://joinmatrix.org/servers/)), and be invited to chat rooms or direct messages as usual.
***

# Using matrix
#### How do you tell people a room address? {#share-room}
With the "https://matrix.to/..." link, which you can see under the i-symbol for the room properties and another click on "share room".
***

#### How can I as an admin delete many messages at once? {#delete-multiple-messages}
Please contact the [GWDG Support](https://gwdg.de/support).
***

#### Sometimes I see a bold marked room and click on it, but yet I don't have the time to immediately edit the content and any consequences for me. How can I mark the room as "unread" again? {#mark-room-as-unread}
Unfortunately, this is not possible in Element. As an interim solution, you can mark the room as a favorite and note to yourself that your own favorites should be looked at again.
***


# "Can I..?" (Features etc.)
#### Can I write LaTeX? {#latex}
Yes! But it is an experimental feature, you can turn it on in `Settings` -> `Labs` -> `Messaging` and then write latex between dollar signs: `$\LaTeX$`.
***

#### Is there such a thing as threads (as in Rocket.Chat/ Slack) in matrix? {#threads}
Yes, matrix supports the use of threads. However, these are still quite new and not optimally usable in all clients.
***

#### I have multiple accounts, can I have messages forwarded from one to the other? {#forward-account}
Not without further ado, no. Technically it is doable, but only with some prior knowledge. We do not actively support such scenarios.
***

#### Can I hold video conferences in matrix? {#videoconf-in-matrix}
At the moment, only 1:1 calls (also with video) are supported. In a few months, group calls with a generally unlimited number of participants might also be possible. It remains to be tested how many camera images can be used simultaneously then.

A very preliminary version is already available, you can switch it on in `Settings` -> `Labs`.

We strongly suggest to use the [GWDG BBB service](https://academiccloud.de/services/bigbluebutton/).
***

#### Is it possible to send files via matrix? / What is the maximum file size that can be sent via matrix? {#file-upload}
In this matrix service, currently uploading of files up to 250 megabytes is allowed. For users at other operators who have set a lower limit, it might not be possible to download files larger than their limit. Generally, the maximum size for most operators is 200 megabytes.

In general we suggest to use [den Academic Cloud Service based on ownCloud](https://academiccloud.de/services/owncloud/) or. [GWDG FileSender](https://filesender.gwdg.de/) for file transfers.
***

#### Can I install a matrix app on my phone without getting notifications? {#app-without-notifications}
Yes, most apps allow you to turn off notifications completely. This is possible in the settings of the respective app.

You can also selectively turn off notifications for particularly large/busy/unimportant chat rooms, this is usually done by long-pressing on the desired room in the room list and then making the notification settings at the bottom or top of the screen (in Element, 4 possible notification levels appear at the bottom of the screen).
***

#### Is it possible to be notified when there are new messages in matrix without opening an app/website? {#notifications-via-email}
Yes, it is possible to receive emails when there are new messages or room invitations in your matrix account. More info can be found [here](/en/settings).
***

#### Can I manage multiple matrix accounts with Element (multi-account client)? {#multiple-accounts-element}
An Element window can currently manage only one matrix account. However, you can, for example, use different clients for the different accounts, including [SchildiChat](https://schildi.chat/), which is very similar to Element. In addition, there are clients, such as [FluffyChat](https://fluffychat.im/) or [Fractal](https://matrix.org/ecosystem/clients/fractal/), which can manage multiple accounts in just one app (or browser tab).

It is also possible to start several Element windows with different matrix accounts, even in the autostart of the computer. To do this, modify the program call to open a specific profile:
```
element-desktop --profile PROFILENAME
```
This way several starters can be placed in the autostart, which then have different profile names, e.g. --profile acloud and --profile PRIVATE. Unfortunately both open windows have the same looking icons in the indicator applet.
***

#### Can I use (chat)bots, Webhooks or RSS-Feeds in Matrix? {#hook}
It is possible, please check the page about [automations and bots](/automations). For simple cases often the `hookshot` user will be enough, for more general cases also a bot-account may be used.

***
