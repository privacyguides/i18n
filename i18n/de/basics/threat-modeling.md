---
meta_title: "Modellierung von Bedrohungen: Der erste Schritt auf deinem Weg zu Privatsphäre - Privacy Guides"
title: "Threat Modeling"
icon: 'material/target-account'
description: Das Gleichgewicht zwischen Sicherheit, Datenschutz und Benutzerfreundlichkeit ist eine der ersten und schwierigsten Aufgaben, die du auf deinem Weg zu Privatsphäre bewältigen musst.
---

Das Gleichgewicht zwischen Sicherheit, Datenschutz und Benutzerfreundlichkeit ist eine der ersten und schwierigsten Aufgaben, die du auf deinem Weg zu Privatsphäre bewältigen musst. Alles ist ein Kompromiss: Je sicherer etwas ist, desto einschränkender oder unbequemer ist es in der Regel, usw. Oft stellen Menschen fest, dass das Problem mit den empfohlenen Werkzeugen darin besteht, dass sie einfach zu schwer zu verwenden sind!

Wenn du die **aller sichersten** verfügbaren Werkzeuge nutzen möchtest, müsstest du *sehr viel* an Benutzerfreundlichkeit opfern. Und selbst dann gilt: ==Nichts ist jemals völlig sicher.== Es gibt **hohe** Sicherheit, aber niemals **vollständige** Sicherheit. Deshalb sind Bedrohungsmodelle (Threat Models) so wichtig.

**Was sind diese Bedrohungsmodelle überhaupt?**

==Ein Bedrohungsmodell ist eine Liste der wahrscheinlichsten Bedrohungen für deine Sicherheits- und Privatsphäre-Bemühungen.== Da es unmöglich ist, sich gegen **jeden** Angriff (oder Angreifer) zu schützen, solltest du dich auf die **wahrscheinlichsten** Bedrohungen konzentrieren. In der Computersicherheit ist eine Bedrohung ein Ereignis, das deine Bemühungen, privat und sicher zu bleiben, untergraben könnte.

Durch die Konzentration auf die Bedrohungen, die für dich relevant sind, wird dein Denken über den notwendigen Schutz eingeengt, sodass du die richtigen Werkzeuge für die Aufgabe auswählen kannst.

## Erstellung deines Bedrohungsmodells

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

Um diese Frage zu beantworten, ist es wichtig festzustellen, wer dich oder deine Informationen angreifen könnte. ==Eine Person oder Einrichtung, die eine Bedrohung für deine Wertsachen darstellt, ist ein „Gegner“ (Adversary).== Beispiele für potenzielle Gegner sind dein Chef, dein Ex-Partner, deine Geschäftskonkurrenz, deine Regierung oder ein Hacker in einem öffentlichen Netzwerk.

*Erstelle eine Liste deiner Gegner oder derjenigen, die versuchen könnten, an deine Wertsachen zu gelangen. Deine Liste kann Einzelpersonen, eine Regierungsbehörde oder Unternehmen enthalten.*

Je nachdem, um wen es sich bei deinen Gegnern handelt, möchtest du diese Liste vielleicht vernichten, nachdem du dein Bedrohungsmodell entwickelt hast.

### Wie wahrscheinlich ist es, dass ich es schützen muss?

==Risiko ist die Wahrscheinlichkeit, dass eine bestimmte Bedrohung gegen eine bestimmte Wertsache tatsächlich eintritt.== Es hängt eng mit den Fähigkeiten deiner Gegner zusammen. Während dein Mobilfunkanbieter die Fähigkeit hat, auf alle deine Daten zuzugreifen, ist das Risiko, dass er deine privaten Daten online veröffentlicht, um deinen Ruf zu schädigen, gering.

Es ist wichtig, zwischen dem, was passieren könnte, und der Wahrscheinlichkeit, dass es passiert, zu unterscheiden. Zum Beispiel besteht die Bedrohung, dass dein Gebäude einstürzt, aber das Risiko ist in San Francisco (wo Erdbeben häufig sind) viel höher als in Stockholm (wo sie selten sind).

Die Risikobewertung ist ein persönlicher und subjektiver Prozess. Viele Menschen finden bestimmte Bedrohungen unannehmbar, egal wie wahrscheinlich sie sind, weil die bloße Anwesenheit der Bedrohung nicht den Aufwand wert ist. In anderen Fällen missachten Menschen hohe Risiken, weil sie die Bedrohung nicht als Problem betrachten.

*Schreibe auf, welche Bedrohungen du ernst nehmen wirst und welche zu selten oder zu harmlos (oder zu schwierig zu bekämpfen) sind, um sich Sorgen zu machen.*

### Wie schlimm sind die Folgen, wenn ich scheitere?

Es gibt viele Möglichkeiten, wie ein Angreifer Zugriff auf deine Daten erhalten kann. Zum Beispiel kann ein Angreifer deine privaten Kommunikationen lesen, wenn sie durch das Netzwerk gehen, oder deine Daten löschen oder beschädigen.

==Die Motive von Angreifern sind sehr unterschiedlich, ebenso wie ihre Taktiken.== Eine Regierung, die die Verbreitung eines Videos, das Polizeigewalt zeigt, verhindern will, begnügt sich vielleicht damit, das Video zu löschen oder seine Verfügbarkeit zu verringern. Im Gegensatz dazu könnte ein politischer Gegner sich Zugang zu geheimen Inhalten verschaffen und diese ohne dein Wissen veröffentlichen wollen.

Die Sicherheitsplanung beinhaltet das Verständnis, wie schlimm die Folgen sein könnten, wenn ein Gegner erfolgreich Zugriff auf eines deiner Wertgegenstände erhält. Um dies zu bestimmen, solltest du die Fähigkeiten deines Gegners berücksichtigen. Beispielsweise hat dein Mobilfunkanbieter Zugriff auf alle deine Telefondaten. Ein Hacker in einem offenen WLAN-Netzwerk kann auf deine unverschlüsselten Kommunikationen zugreifen. Deine Regierung könnte stärkere Fähigkeiten haben.

*Schreibe auf, was deine Gegner mit deinen privaten Daten machen könnten.*

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

- [Häufige Ziele und Bedrohungen :material-arrow-right-drop-circle:](common-threats.md)

## Quellen

- [EFF Surveillance Self Defense: Your Security Plan](https://ssd.eff.org/en/module/your-security-plan)
