---
meta_title: "Modellierung von Bedrohungen: Der erste Schritt auf Ihrem Weg zum Datenschutz - Privacy Guides"
title: "Threat Modeling"
icon: 'material/target-account'
description: Das Gleichgewicht zwischen Sicherheit, Datenschutz und Benutzerfreundlichkeit ist eine der ersten und schwierigsten Aufgaben, die du auf deinem Weg zu Privatsphäre bewältigen musst.
---

Das Gleichgewicht zwischen Sicherheit, Datenschutz und Benutzerfreundlichkeit ist eine der ersten und schwierigsten Aufgaben, die du auf deinem Weg zu Privatsphäre bewältigen musst. Alles ist ein Kompromiss: Je sicherer etwas ist, desto einschränkender oder unbequemer ist es in der Regel, usw. Oft stellen Menschen fest, dass das Problem mit den empfohlenen Werkzeugen darin besteht, dass sie einfach zu schwer zu verwenden sind!

Wenn du die **aller sichersten** verfügbaren Werkzeuge nutzen möchtest, müsstest du *viel* an Benutzerfreundlichkeit opfern. Und selbst dann gilt: ==Nichts ist jemals völlig sicher.== Es gibt **hohe** Sicherheit, aber niemals **vollständige** Sicherheit. Deshalb sind Threat Models (bzw. Bedrohungsmodelle) so wichtig.

**Was sind diese Bedrohungsmodelle überhaupt?**

==Ein Bedrohungsmodell ist eine Liste der wahrscheinlichsten Bedrohungen für deine Sicherheits- und Privatsphäre-Bemühungen.== Da es unmöglich ist, sich gegen **jeden** Angriff (oder Angreifer) zu schützen, solltest du dich auf die **wahrscheinlichsten** Bedrohungen konzentrieren. In der Computersicherheit ist eine Bedrohung ein Ereignis, das deine Bemühungen, privat und sicher zu bleiben, untergraben könnte.

Durch die Konzentration auf die Bedrohungen, die für dich relevant sind, wird dein Denken über den notwendigen Schutz eingeengt, sodass du die richtigen Werkzeuge für die Aufgabe auswählen kannst.

## Creating Your Threat Model

Um herauszufinden, was mit den Dingen, die dir wichtig sind, passieren könnten und vor wem du sie schützen musst, solltest du diese fünf Fragen beantworten:

1. Was will ich schützen?
2. Vor wem möchte ich es schützen?
3. Wie wahrscheinlich ist es, dass ich es schützen muss?
4. Wie schlimm sind die Folgen, wenn ich scheitere?
5. Wie viel Mühe bin ich bereit, aufzubringen, um diese Konsequenzen zu verhindern?

### Was will ich schützen?

Ein „Wertgegenstand“ (Asset) ist etwas, das du schätzt und schützen möchtest. Im Kontext der digitalen Sicherheit ==ist ein solcher Wertgegenstand in der Regel eine Art von Information.== Zum Beispiel sind deine E-Mails, Kontaktlisten, Sofortnachrichten, Standort und Dateien alle mögliche Wertsachen. Auch deine Geräte selbst können Wertgegenstände sein.

*Mach eine Liste deiner Wertsachen: Daten, die du speicherst, wo sie gespeichert sind, wer Zugriff darauf hat und was andere daran hindert, darauf zuzugreifen.*

### Vor wem möchte ich es schützen?

To answer this question, it's important to identify who might want to target you or your information. ==A person or entity that poses a threat to your assets is an “adversary”.== Examples of potential adversaries are your boss, your former partner, your business competition, your government, or a hacker on a public network.

*Make a list of your adversaries or those who might want to get ahold of your assets. Your list may include individuals, a government agency, or corporations.*

Depending on who your adversaries are, this list might be something you want to destroy after you've finished developing your threat model.

### Wie wahrscheinlich ist es, dass ich es schützen muss?

==Risk is the likelihood that a particular threat against a particular asset will actually occur.== It goes hand-in-hand with capability. While your mobile phone provider has the capability to access all of your data, the risk of them posting your private data online to harm your reputation is low.

It is important to distinguish between what might happen and the probability it may happen. For instance, there is a threat that your building might collapse, but the risk of this happening is far greater in San Francisco (where earthquakes are common) than in Stockholm (where they are not).

Assessing risks is both a personal and subjective process. Many people find certain threats unacceptable, no matter the likelihood they will occur, because the mere presence of the threat is not worth the cost. In other cases, people disregard high risks because they don't view the threat as a problem.

*Write down which threats you are going to take seriously, and which may be too rare or too harmless (or too difficult to combat) to worry about.*

### Wie schlimm sind die Folgen, wenn ich scheitere?

There are many ways that an adversary could gain access to your data. For example, an adversary can read your private communications as they pass through the network, or they can delete or corrupt your data.

==The motives of adversaries differ widely, as do their tactics.== A government trying to prevent the spread of a video showing police violence may be content to simply delete or reduce the availability of that video. In contrast, a political opponent may wish to gain access to secret content and publish that content without you knowing.

Security planning involves understanding how bad the consequences could be if an adversary successfully gains access to one of your assets. To determine this, you should consider the capability of your adversary. For example, your mobile phone provider has access to all of your phone records. A hacker on an open Wi-Fi network can access your unencrypted communications. Your government might have stronger capabilities.

*Write down what your adversary might want to do with your private data.*

### Wie viel Mühe bin ich bereit, aufzubringen, um diese Konsequenzen zu verhindern?

==Es gibt keine perfekte Sicherheitslösung.== Nicht jeder hat die gleichen Prioritäten, Bedenken oder den gleichen Zugang zu Ressourcen. Deine Risikobewertung wird es dir ermöglichen, die richtige Strategie für dich zu planen, indem du Bequemlichkeit, Kosten und Privatsphäre in Einklang bringst.

Zum Beispiel könnte ein Anwalt, der einen Mandanten in einem Fall der nationalen Sicherheit vertritt, bereit sein, größere Anstrengungen zu unternehmen, um die Kommunikation über diesen Fall zu schützen, wie zum Beispiel die Verwendung von verschlüsselten E-Mails, als eine Mutter, die ihrer Tochter regelmäßig lustige Katzenvideos per E-Mail schickt.

*Schreibe auf, welche Optionen dir zur Verfügung stehen, um deine einzigartigen Bedrohungen zu mindern. Notiere, ob du finanzielle Einschränkungen, technische Einschränkungen oder soziale Einschränkungen hast.*

### Probiere es selbst: Schütze dein Hab und Gut

Diese Fragen lassen sich auf eine Vielzahl von Situationen anwenden, online und offline. Als allgemeine Demonstration, wie diese Fragen funktionieren, lass uns einen Plan erstellen, um dein Haus und deine Besitztümer sicher zu halten.

**Was möchtest du schützen? (Oder: *Was hast du, das es wert ist, geschützt zu werden?*)**
:

Deine Wertsachen könnten Schmuck, elektronische Geräte, wichtige Dokumente oder Fotos sein.

**Vor wem möchtest du es schützen?**
:

Zu deinen Gegnern könnten Einbrecher, Mitbewohner oder Gäste zählen.

**Wie wahrscheinlich ist es, dass du sie schützen musst?**
:

Hat deine Nachbarschaft eine Geschichte von Einbrüchen? Wie vertrauenswürdig sind deine Mitbewohner oder Gäste? Welche Fähigkeiten haben deine Gegner? Welche Risiken solltest du in Betracht ziehen?

**Wie schlimm sind die Folgen, wenn du scheiterst?**
:

Hast du etwas in deinem Haus, das du nicht ersetzen kannst? Hast du die Zeit oder das Geld, um diese Dinge zu ersetzen? Hast du eine Versicherung, die gestohlene Waren aus deinem Haus abdeckt?

**Wie viel Mühe bist du bereit, aufzubringen, um diese Konsequenzen zu verhindern?**
:

Bist du bereit, einen Safe für sensible Dokumente zu kaufen? Kannst du es dir leisten, ein hochwertiges Schloss zu kaufen? Hast du Zeit, ein Schließfach in deiner örtlichen Bank zu eröffnen und deine Wertsachen dort aufzubewahren?

Nur wenn du dir diese Fragen gestellt hast, wirst du in der Lage sein, zu beurteilen, welche Maßnahmen du ergreifen solltest. Wenn deine Besitztümer wertvoll sind, die Wahrscheinlichkeit eines Einbruchs jedoch gering ist, möchtest du vielleicht nicht zu viel Geld in ein Schloss investieren. Wenn die Wahrscheinlichkeit eines Einbruchs jedoch hoch ist, solltest du das beste Schloss auf dem Markt besorgen und in Betracht ziehen, ein Sicherheitssystem hinzuzufügen.

Einen Sicherheitsplan zu erstellen, wird dir helfen, die Bedrohungen zu verstehen, die einzigartig für dich sind, und deine Wertgegenstände, deine Gegner und die Fähigkeiten deiner Gegner sowie die Wahrscheinlichkeit der Risiken, denen du ausgesetzt bist, zu bewerten.

## Weitere Informationen

Für Menschen, die ihre Privatsphäre und Sicherheit online erhöhen möchten, haben wir eine Liste von häufigen Bedrohungen zusammengestellt, mit denen unsere Besucher konfrontiert sind, oder von Zielen, die unsere Besucher verfolgen. Diese Liste soll dir Inspiration geben und die Grundlage unserer Empfehlungen veranschaulichen.

- [Gemeinsame Ziele und Bedrohungen :material-arrow-right-drop-circle:](common-threats.md)

## Quellen

- [EFF Surveillance Self Defense: Your Security Plan](https://ssd.eff.org/en/module/your-security-plan)
