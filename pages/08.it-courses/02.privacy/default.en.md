---
title: 'Communicating with Others'
---

Communication resources and the internet have mad communicating with others easier than ever before, but have increased surveillance to levels unheard of in human history.  Without taking extra measures to protect your privacy, every phone call, text message, email, IM, videochat, etc... can be vulnerable to spying.

Often, the most secure way to communicate with others is in person, without computers or telephones.  However, this is not always possible.  The best thing to do is to use comprehensive data encryption if you communicate online and need to protect the content of your communication.


# How Comprehensive Encryption Works!

When two people want to communicate in a secure manner (Akiko and Boris, for example), they have to generate cryptographic keys.  Before Akiko sends a message to Boris, she has to encrypt it using the key, ensuring that only Boris will be able to read it.  She then sends the encrypted message on the internet.  If somebody is monitoring Akiko and Boris, and even if they have access to the service Akiko used to send the message (like her email account), they will not be able to see anything except for the encrypted data and will not be able to read the message.  When Boris receives the message, he can use the code to decypher the message and make it readable.

Data encryption requires a certain effort, but it is the only method users can ensure that their communications remain secret and allows them to have confidence in the platforms they use.  Certain services, like Skype, [claim](https://support.skype.com/en/faq/FA31/does-skype-use-encryption?q=data+encryption) to offer comprehensive encryption, but it is not really so.  In order for the encryption to truly be secure, users have to have the power to verify that the crypto key being used to encode the messages is available only to the person or people it is supposed to be available to, and nobody else.  If the application does not have this built-in capacity, all encryption can be intercepted by the service provider itself (if a government requests the information, for example).

You can read the white paper ["Encryption Works"](https://cavallette.noblogs.org/files/2013/09/encryption_works.pdf) from the Freedom of the Press Foundation to get detailed instructions about how to use encryption to protect instant messages and emails.  Make sure to also consult the following modules about self-protection from digital surveillance:

-   [Introduction to Public Key Cryptography and PGP](/en/module/introduction-public-key-cryptography-and-pgp)
-   [How to Use OTR on Windows](/en/module/how-use-otr-windows)
-   [How to Use OTR on Mac](/en/module/how-use-otr-mac)


Voice Calls
-------------

When you call somebody, whetheer from a landline or cell phone, your call is not encrypted in its entirety.  If you use a cell phone, your call can be (weakly) encrypted between the handset and relay antennas.  However, if your call travels over the phone network, it is vulnerable to interception from your service provider and thus, by governments and organizations that regulate and inspect the phone company.  The easiest way to ensure your conversations are encrypted is to use VoIP.

Use caution!  The most well known providers of VoIP, such as Skype and Google Hangouts, offer encryption that prevents outside spies from listening to your conversation, but *the provider itself can still listen to your conversation*.  Depending on the nature of your threat, this may or may not be a problem.

Certain services that offer complete VoIP encryption include:

-   [Ostel](https://ostel.co/)
-   [RedPhone](/en/module/how-use-redphone-android)
-   [Silent Phone](https://silentcircle.com/services#mobile)
-   [Signal for iPhone](/en/module/how-use-signal-%E2%80%93-private-messenger)
-   [Signal for Android](https://ssd.eff.org/fr/node/93)

In order to have conversations completely encrypted by VoIP, the two parties need to use the same program (or compatible programs).

Text Messages
-----------------

SMS does not provide an end-to-end encryption solution.  If you would like to send encrypted text messages from your telephone, you need to use an encrypted instant messaging application, instead of SMS.

Some encrypted instant messaging applications use their own protocol.
 - Users of [Signal](https://ssd.eff.org/fr/node/61/) on Android and iOS can talk in a secure manner with other users of the program
 -  [ChatSecure](https://ssd.eff.org/fr/node/51) is an application that encrypts your conversations with OTR on all types of networks that use XMPP, meaning you can choose from a wide array of independent messaging services.

Instant Messaging
--------------------

- Off-the-Record (OTR) is a protocol to encrypt text conversations in real time, and can be used with numerous services. 

Some tools that incorporate OTR in their instant messaging include:

-   [Pidgin](https://ssd.eff.org/fr/module/instructions-utiliser-otr-pour-windows) (for Windows or Linux)
-   [Adium](https://ssd.eff.org/fr/node/40/) (for OS X)
-   [ChatSecure](https://ssd.eff.org/fr/node/51/) (for iPhone and Android)


E-mails
-------
The majority of email providers let you access your emails using a web browser, like Chrome or Firefox.  The vast majority provide support for HTTPS, or the encryption layer.  You can tell if your email provider accepts HTTPS if you connect to it by using a URL that starts with HTTPS:// instead of HTTP:// (for example: <https://mail.google.com> is the URL for gmail).

If your service provider accepts HTTPS, but is not the default setting, try to replace HTTP with HTTPS in the URL, and refresh the page.  If you want to ensure that you always use HTTPS on available sites, download [the HTTPS Everywhere extension](https://www.eff.org/https-everywhere) for Firefox or Chrome.

Certain email providers use HTTPS by default, including:

-   Gmail
-   Riseup
-   Yahoo

Several others offer the option to use HTTPS by default in the settings.  Hotmail is the most well-known service with this approach.

What are the consequences of encryption of the transport layer, and why might you need it?  HTTPS, also known as SSL (Secure Sockets Layer) or TLS (Transport Layer Security), encrypts your messages in a way that prevents anybody else from reading them on your network.  This can mean people using the same WiFi in an airport or café, other people in your office or school, administrators of your internet service provider, malicious internet pirates, governments, or law-enforcement officers.  If you use HTTP instead of HTTPS, attackers can intercept and view your search history, the content of your emails, blog posts, messages, etc...

HTTPS is the most basic level of encryption that we recommend for navigating the Web.  It is as elementary as putting on your seatbelt when you drive.

But HTTPS cannot do everything.  When you send emails using HTTPS, your email provider still gets a non-encrypted copy of the message.  Governments and law enforcement organizations can get access to this data with a warrant.  In the United States, the majority of email providers have a policy of informing you any time there is a request from the government for your data.  But these policies are strictly voluntary and, in many cases, the providers are legally prohibited from informing you of a request.  Some providers, like Google, Yahoo, and Microsoft publish full transparency reports, in which they state the number of data requests that they received from governments, the countries these requests originated from, and the frequency with which the country complied with the request and released data.

If your threat model includes a government or law-enforcement agency, or you have other reasons to assure that your provider cannot share the contents of your communication with a third-party, you may want to consider comprehensive encryption software for your emails.

PGP (Pretty Good Privacy) is the standard encryption software for your emails.  Correctly used, it offers very strong protection for your communications.  For detailed instructions on how to install and use PGP encription for your email, see:

-   [How to use PGP on Mac OSX](/en/module/how-use-pgp-mac-os-x)
-   [How to use PGP on Windows](/en/module/how-use-pgp-windows-pc)
-   [How to use PGP on Linux](/en/module/how-use-pgp-linux)


## What Comprehensive Encryption Cannot Do
Global encryption exclusively protects the content of your communications, not the communication data itself.  It does not protect your meta-data.  That means that other data (such as the subject of the email, who it is sent to, and when it is sent) can still be collected.

Meta-data can provide extremely revealing and valuable information about you, even when the content of your communications remains secret.

Meta-data relating to your phone calls can divulge certain sensible and private information. For example:

-  It can tell that you called a phone-sex service at 2:24 am and were on the phone for 18 minutes, but cannot tell what you talked about.
-  It can tell that you called a suicide hotline from the Golden Gate Bridge, but the subject of your call remains secret.
-  It can tell that you called an HIV testing service, then your doctor, then your health insurance company all in one hour, but it doesn't know what you discussed.
-  It knows that you received a call from the NRA while it was running a campaign against anti-gun legislation, and that you called your senators and representatives in Congress immediately afterward, but the content of these calls remains secure against surveillance.
-  It can tell that you called a gynecologist, talked for a half hour, then called Planned Parenthood later in the day, but nobody can tell what you talked about.

If you call using a cell phone, *location information is included in the meta-data*.  In 2009, Malte Spitz, a Green Party politican, sued German company Deutsche Telekom to get all the information the company knew about him.  He then sent the information to a Germany newspaper.  The [resulting visualization](http://www.zeit.de/datenschutz/malte-spitz-data-retention/) illustrates in incredible detail Spitz's movements over those six months.

Protecting your meta-data requires the usage of other tools, such as [Tor](/en/module/how-use-tor-windows#overlay=en/node/57/), with global encryption.

In order to visualize the manner in which Tor and HTTPS work together to protect your communications and meta-data against potential attacks, you can see [this explanation](https://www.eff.org/pages/tor-and-https).

Text originally published on https://ssd.eff.org/fr/playlist/souhaitez-vous-un-pack-de-s%C3%A9curit%C3%A9-pour-d%C3%A9butants#communiquer-avec-les-autres under CC BY license.
