---
meta_title: "Warum E-Mail nicht die beste Wahl für Privatsphäre und Sicherheit ist - Privacy Guides"
title: E-Mail-Sicherheit
icon: material/email
description: E-Mail ist von Natur aus in vielerlei Hinsicht unsicher. Hier sind einige Gründe, warum sie nicht unsere erste Wahl für sichere Kommunikation ist.
---

E-Mail ist von Natur aus eine unsichere Form der Kommunikation. Du kannst deine E-Mail-Sicherheit mit Tools wie OpenPGP verbessern, die Ende-zu-Ende-Verschlüsselung zu deinen Nachrichten hinzufügen, aber OpenPGP hat im Vergleich zur Verschlüsselung in anderen Messaging-Anwendungen eine Reihe von Nachteilen. Auch können einige E-Mail-Daten aufgrund der Art und Weise, wie E-Mails konzipiert sind, niemals von sich aus verschlüsselt werden.

Daher sind E-Mails am besten geeignet, um Transaktions-E-Mails (wie Benachrichtigungen, Bestätigungs-E-Mails, Passwortrücksetzungen usw.) von den Online-Diensten zu empfangen, für die du dich anmeldest, und nicht für die Kommunikation mit anderen.

## Übersicht zur E-Mail-Verschlüsselung

Die Standardmethode zum Hinzufügen von E2EE zu E-Mails zwischen verschiedenen E-Mail-Anbietern ist die Verwendung von OpenPGP. Es gibt verschiedene Implementierungen des OpenPGP-Standards, die bekanntesten sind [GnuPG](https://de.wikipedia.org/wiki/GNU_Privacy_Guard) und [OpenPGP.js](https://openpgpjs.org).

Es gibt noch einen anderen, bei Unternehmen beliebten Standard namens [S/MIME](https://de.wikipedia.org/wiki/S/MIME), für den jedoch ein von einer [Zertifizierungsstelle](https://de.wikipedia.org/wiki/Zertifizierungsstelle_(Digitale_Zertifikate)) ausgestelltes Zertifikat erforderlich ist (nicht alle von diesen stellen S/MIME-Zertifikate aus). Es wird von [Google Workplace](https://support.google.com/a/topic/9061730) und [Outlook für Web oder Exchange Server 2016, 2019](https://support.microsoft.com/de-de/topic/verschl%C3%BCsseln-von-nachrichten-mit-s-mime-in-outlook-im-web-878c79fc-7088-4b39-966f-14512658f480) unterstützt.

Selbst wenn du OpenPGP verwendest, unterstützt es keine [Forward Secrecy](https://de.wikipedia.org/wiki/Perfect_Forward_Secrecy), d. h. wenn entweder dein privater Schlüssel oder der des Empfängers gestohlen wird, sind alle vorherigen Nachrichten, die damit verschlüsselt wurden, offengelegt. Aus diesem Grund empfehlen wir [Instant Messenger](../real-time-communication.md) mit Forward Secrecy, für persönliche Kommunikation, wann immer möglich, anstelle von E-Mails.

## Was ist der Web Key Directory Standard?

Der Web Key Directory (WKD) Standard ermöglicht es E-Mail-Clients, den OpenPGP-Schlüssel für andere Postfächer zu ermitteln, auch wenn diese bei einem anderen Anbieter gehostet werden. E-Mail-Clients, die WKD unterstützen, fragen den Server des Empfängers nach einem Schlüssel, der auf dem Domainnamen der E-Mail-Adresse basiert. Wenn du beispielsweise eine E-Mail an `jonah@privacyguides.org` sendest, fragt dein E-Mail-Programm bei `privacyguides.org` nach dem OpenPGP-Schlüssel von Jonah, und falls `privacyguides.org` einen Schlüssel für dieses Konto hat, wird deine Nachricht automatisch verschlüsselt.

Neben den [von uns empfohlenen E-Mail-Clients](../email-clients.md), die WKD unterstützen, gibt es auch einige Webmail-Anbieter, die WKD unterstützen. Ob *dein eigener* Schlüssel für andere bei WKD veröffentlicht wird, hängt von deiner Domainkonfiguration ab. Verwendest du einen [E-Mail-Anbieter](../email.md#openpgp-compatible-services), der WKD unterstützt, wie z. B. Proton Mail oder Mailbox.org, können diese deinen OpenPGP-Schlüssel auf ihrer Domain für dich veröffentlichen.

Um deine eigene Domain zu verwenden, musst du WKD separat konfigurieren. Kontrollierst du deinen Domainnamen, kannst du WKD unabhängig von deinem E-Mail-Anbieter einrichten. Eine einfach Möglichkeit das zu tun, ist die Nutzung der Funktion „[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)“ von keys.openpgp.org, indem du einen CNAME-Eintrag auf der `openpgpkey-Subdomain` deiner Domain setzt, der auf `wkd.keys.openpgp.org` zeigt, und dann deinen Schlüssel auf [keys.openpgp.org](https://keys.openpgp.org) hochlädst. Alternativ kannst du [WKD selbst auf deinem Webserver hosten](https://wiki.gnupg.org/WKDHosting).

Wenn du eine gemeinsam genutzte Domain eines Anbieters verwendest, welcher WKD nicht unterstützt, wie z.B. @gmail.com, kannst du deinen OpenPGP-Schlüssel auf diese Weise nicht mit anderen teilen.

### Welche E-Mail-Clients unterstützen E2EE?

E-Mail-Anbieter, die dir die Verwendung von Standard-Zugriffsprotokollen wie IMPA und SMTP ermöglichen, können mit jedem der [von uns empfohlenen E-Mail-Clients](../email-clients.md) verwendet werden. Abhängig von der Authentifizierungsmethode kann dies zu einer Verringerung der Sicherheit führen, wenn entweder der Anbieter oder der E-Mail-Client OATH oder eine Bridge-Anwendung nicht unterstützt, da eine [Multi-Faktor-Authentifizierung](multi-factor-authentication.md) mit einer reinen Passwort-Authentifizierung nicht möglich ist.

### Wie schütze ich meine privaten Schlüssel?

Eine Smartcard (wie z. B. ein [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) oder [Nitrokey](../security-keys.md#nitrokey)) funktioniert, indem sie eine verschlüsselte E-Mail-Nachricht von einem Gerät (Telefon, Tablet, Computer usw.) empfängt, auf dem ein E-Mail-/Webmail-Client läuft. Die Nachricht wird dann von der Smartcard entschlüsselt und der entschlüsselte Inhalt an das Gerät zurückgeschickt.

Es ist vorteilhaft, wenn die Entschlüsselung auf der Smartcard erfolgt, um zu vermeiden, dass dein privater Schlüssel möglicherweise einem kompromittierten Gerät preisgegeben wird.

## Übersicht über E-Mail-Metadaten

E-Mail-Metadaten werden in dem [Header-Abschnitt](https://de.wikipedia.org/wiki/Header_(E-Mail)) der E-Mail gespeichert und enthalten einige sichtbare Header-Zeilen, die du vielleicht schon gesehen hast, wie z. B.: `An`, `Von`, `Cc`, `Datum`, `Betreff`. Viele E-Mail-Clients und -Anbieter fügen außerdem eine Reihe von versteckten Header-Zeilen hinzu, die Informationen über dein Konto preisgeben können.

E-Mail-Programm können Metadaten verwenden, um anzuzeigen, von wem eine Nachricht stammt und wann sie empfangen wurde. Server können sie verwenden, um zu bestimmen, wohin eine E-Mail gesendet werden muss, neben [anderen Zwecken](https://en.wikipedia.org/wiki/Email#Message_header), die nicht immer transparent sind.

### Wer kann E-Mail-Metadaten einsehen?

Die E-Mail-Metadaten sind mit [Opportunistic TLS](https://de.wikipedia.org/wiki/Opportunistic_TLS) (dt.: STARTTLS) vor externen Beobachtern geschützt, können aber dennoch von deinem E-Mail-Client-Programm (oder Webmail) und allen Servern, die die Nachricht von dir an beliebige Empfänger weiterleiten, einschließlich deines E-Mail-Anbieters, eingesehen werden. Manchmal verwenden E-Mail-Server auch Dienste von Drittanbietern zum Schutz vor Spam, die in der Regel auch Zugang zu deinen Nachrichten haben.

### Warum können Metadaten nicht E2EE werden?

E-Mail-Metadaten sind entscheidend für die grundlegenden Funktionen von E-Mails (woher sie kommen und wohin sie gehen sollen). E2EE war ursprünglich nicht in den E-Mail-Protokollen enthalten, sondern erfordert zusätzliche Software wie OpenPGP. Da OpenPGP-Nachrichten mit herkömmlichen E-Mail-Anbietern zusammenarbeiten müssen, kann es keine E-Mail-Metadaten verschlüsseln, sondern nur den eigentlichen Nachrichtentext. Das bedeutet, dass selbst bei Verwendung von OpenPGP Außenstehende viele Informationen über deine Nachrichten sehen können, z. B. an wen du eine E-Mail sendest, die Betreffzeilen, wann du sie sendest usw.
