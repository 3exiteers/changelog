# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

- Internationalization
- Overview of available stories
- Overview of available quests
- Online editor for events, stories and quests
- Quest ranomizer to randomized displayed quest
- Github repository selection
- User/profile management
- Wordcloud input
- Feedback link
- Event QR codes (via permanent link)
- Sync of team players
- "Waiting points" (to ensure all players in the same position) in story

## [201-10-24] - 2021-10-24

### Added

- Dei Aktualisierungen über Github wurden weiter optimiert. Repositories in der 3Exiteers Organisation rufen nun per Webhook die Aktualisierungs-Funktion auf, mit der die aktualisierten Repositories für Èvebt`, `Story`und `Quest` automatisch und nur für dieses Repository aktualsisiert werden. Änderungen an den Repositories werden dadurch umgehend angewendet. Der bisherige Aktualisierungsmechanismus steht weiterhin zur Verfügung.

## [201-10-23] - 2021-10-23

### Fixed

- Der Status der Schaltflächen in einer `#junction` wird nun für die letzte Schaltfläche der Voraussetzungen richtig gesetzt, sollten alle Voraussetzungen erfüllt sein und der Default angezeigt werden.

## [201-10-22] - 2021-10-22

### Added

- BIG UPDATE! Wir haben auf unserer Spieler gehört! Auf vielfachen Wunsch kann nun innerhalb eines Exit Game der Fortschritt erkannt werden. Auf jeder Seite eines Exit Game wird nun die Gesamtanzahl der Kapitel als Segmente angezeigt. Mit dem Fortschritt des Teams in der Geschichte, werden die bereits vom Team erreichten Kapitel gekennzeichnet und mit einem Link versehen. Die Spieler eines Teams haben so die Möglichkeit, die bereits erreichten Kapitel durch Auswahl der Segmente direkt aufzurufen. Damit können nachfolgende Teammitglieder gleich zum letzten vom Team erreichten Kapitel springen oder das Team an ein vorheriges Kapitel zurückspringen. Wir danken allen Hinweisgebern für diese großartige Idee.

## [201-10-19] - 2021-10-19

### Fixed

- Für Hinweis-Punkte kann nun in der `story.json` explizit für einen Hinweis `null` gesetzt werden, sollte ein Hinweis die Punkte aus der `quest.json` nutzen sollen, ein anderer jedoch nicht. Diese Option der expliziten Angabe ist als Ergänzung zu `nonsolution_hint` und `solution_hint` zu sehen.

## [201-10-19] - 2021-10-19

### Added

- Die Funktion `snow` wurde eingebaut, mit der herabfallende Schnellflocken zur Anzeige gebracht werden können. Als Parwemeter zu der Funktion kann die Anzahl der Schneeflocken angegeben werden.

## [201-10-17] - 2021-10-17

### Added

- Die Option `nonsolution_hint` in der `story.json` unterhalb der Punkteanpassungen eines Kapitels ermöglicht nun unabhängig von der Anzahl der Hinweise in einer `quest.json` die Anpassung von Punktekosten für einen normalen Hinweis. Ist die Option `solution:false` gesetzt oder diese Option nicht in der `quest.json` angegeben, überschreibt `nonsolution_hint` die Kosten für jeden normelen Hinweis dieser Quest. So können normale Hinwiese unabhängig von ihrer ID (Position) mit einem - zum Beispiel - abweichenden, aber dafür identischen, Malus belegt werden. (Dank an @Fez)

- Die Option `solution_hint` in der `story.json` unterhalb der Punkteanpassungen eines Kapitels ermöglicht nun unabhängig von der Anzahl der Hinweise in einer `quest.json` die Anpassung von Punktekosten für einen finalen Hinweis. Ist die Option `solution:true` bei einem Hinweis angegeben, überschreibt `solution_hint` die Kosten für diesen Hinweis. So können auflösende Hinwiese unabhängig von ihrer ID (Position) mit einem zum Beispiel höheren Malus belegt werden. (Dank an @Fez)

## [201-10-16] - 2021-10-16

### Added

- Es können nun in der Geschichte minimale und maximale Punkte-Limits eingefügt werden. Diese Limits bewirken, dass der Punktestand der Spielenden nicht unter oder über die angegebenen Werte gezählt wird. (Dank an @Fez)

- Es kann innerhalb der Geschichte und des Events definiert werden, dass inkorrekte Lösungsversuche mit Punktabzug (Malus) berechnet werden. Diese Funktion fördert das Commitment der Spielenden eines Teams für einen Lösungsversuch. (Dank an @Fez)

## [201-10-12] - 2021-10-12

### Added

- Social Media-Links in den Kapitel-Seiten "Registrierung" und "Abschlusskapitel"
- Feedback-Formular in der Kapitel-Seite "Abschlusskapitel"

### Improved

- Internationalisierung der Website weiter ausgebaut

## [201-10-02] - 2021-10-02

### Added

- Die Website und das Framework wurden um Internationalisierungs-Funktionen erweitert, die eine Übersetzung der Inhalte in andere Sprachen erlauben. Der Umbau der Ausgaben auf das internationalisierbare Format wird nun sukzessive fortgeführt.

## [201-09-18] - 2021-09-18

### Improved

- Die Analyse von fehlerhaften Seiten aufrufen wurde optimiert, um die Stabilität des Systems gewährleisten zu können.

## [201-09-17] - 2021-09-17

### Improved

- Es wurden verschiedene statische Dateien auf dem Webserver implementiert, die eine optimierte Integration von Websiten erlauben.

## [201-09-15] - 2021-09-15

### Added

- Die Website ermöglicht nun eine Registrierung und Anmeldung mit einem Benutzerprofil. Dadurch können in den nächsten Entwicklungen rollenbasierte Funktionen implementiert werden. Zudem wird über diese Profile zukünftig die An- und Abmeldung zum/vom Newsletter umgesetzt, so dass ein keine weitere Verifikation der E-Mailadresse erforderlich ist.
 
## [201-09-09] - 2021-09-09

### Improved

- Die Variablen innerhalb der Inhalte (Story) werden nun zusätzlich zu den Definitionen aus den Teams und dem Event aus der Story selber ermittelt. Dabei folgt die Ersetzung der Reihenfolge `team` -> `event` -> `story`. Dieser logische Schritt ist erforderlich, um als Story Creator die eigenen Platzhalter in einer Geschichte vorgeben zu können. Event Creators können als alternative Angaben machen und sich dabei an den Variablen-Definitionen der Story orientieren.

- Die Anzeige des Dialogs für Hinweise wurde überarbeitet, um den Bereich "bisherige Tipps" beim ersten Aufrufe konsistenter darzustellen, sollten noch keine Tipps in Anspruch genommen worden sein.

## [201-09-08] - 2021-09-08

### Added

- Im Design `vfl` wurde die Hinweis-Schaltfläche `Tipps anzeigen` auf Seiten mit Herausforderungen dauerhaft im unteren rechten Bereich eingeblendet. Diese Umsetzung erfolgte auf Grund der Benutzer-Feedbacks aus dem Pilottest zum Format "Hack your way", aus dem deutlich wurde, das Hinweise unter Umständen eher in Anspruch genommen werden, wenn diese Option dem Spielenden deutlicher ist.

## [201-09-05] - 2021-09-05

### Improved

- Die Handhabung von Ausnahmesituationen (Edge cases) bei Aufruf von Events und Stories wurde verbessert und vereinheitlicht.

## [201-09-04] - 2021-09-04

### Added

- Das Exit Game "Hackathon 2021" wurde fertig erstellt und steht die kommenden Tage für einen exklusiven Pilottest zur Verfügung.

## [201-09-01] - 2021-09-01

### Added

- Die Variable `solution` wurde für Quests implementiert, bei der die erste angegebene Lösung aus dem Attribut `solutions` (die immer existieren muss) dynamisch ausgegeben wird. Ein Quest Creator erhält dadurch die Möglichkeit, einen abschließenden Hinweis mit ded Lösung anzugeben, ohne diese anpassen zu müssen, sollte sich die Quest beziehungsweise dessen Lösung geändert hat.

### Changed

- Hinweis vor Anzeige eines auflösenden Hinweises optimiert, so dass der Nutzende sich der weiteren Anzeige bewusst sein sollte :)

## [201-08-29] - 2021-08-29

### Added

- Für Hinweise zu Herausforderungen wurde das Attribut `solution` (`hints` -> id -> `solution`) implementiert, mit dem ein Hinweis markiert werden kann, der die Lösung zeigt. Der Spieler wird auf diesen Umstand explizit hingeweisen.

## [201-08-19] - 2021-08-19

### Added

- Die Funktion `handout` ermöglicht nun innerhalb der Story die Einbindung eines Deckblatts bzw. der ersten Seiten und Abschlussseiten. Zwischen diese Bestandteile werden die Handouts der Quests eingebettet, so dass bei Erzeugung ein in sich schlüssiges PDF generiert wird. 

### Changed

- Verschiedene Quests mit neuen Handouts aktualisiert
- Übertragung von Framework-Einstellungen in die App-Konfiguration
- Länge der Teamcodes auf 20 Zeichen erhöht

## [201-08-16] - 2021-08-16

### Changed

- Updates und Änderungen an der Homeoffice Rätsel-Reihe 

## [201-08-12] - 2021-08-12

### Changed

- Update des Sundisc Rätsels, Game: Flug KLM

## [201-08-11] - 2021-08-11

### Added

- Wir haben jetzt einen Instagram Account, besucht uns doch mal unter @3Exiteers

### Changed

- Änderungen am Exit Game Homeoffice, erstes Rätsel ersetzt und neue Funktionen eingearbeitet
- Vektorisierung der Grafik der Quest 'shiphol' 

## [201-08-09] - 2021-08-09

### Changed

- Die Struktur sämtlicher Stories wurde auf die neue `content`-Struktur angepasst, so dass sich alle Inhalte nun aus dieser Struktur lesen lassen. Dies ist in Vorbereitung zur Umsetzung der sogenannten `branches` erfolgt, so dass alle dargestellten Inhalte einer Seite aus dieser Struktur gelesen werden.

## [201-08-08] - 2021-08-08

### Added

- Die Website wurde um die Funktion `benefits` erweitert, auf der die Vorteile von digitalen Exit Games beschrieben werden.

### Changed

- Die Struktur und die Inhalte der Website wurden aktualisiert.

## [201-08-07] - 2021-08-07

### Added

- Die Website wurde um den Bereich `Features` erweitert. In diesem Bereich werden die Highlights des Frameworks dargestellt und kurz beschrieben.

### Changed

- Die Navigation der Website wurde aktualisiert. Es wurden die Menüeinträge in der oberen Navigation, sowie im Fußbereich, hinsichtlich der Bezeichnung angepasst und auf die aktuellen Funktionen referenziert.

## [201-08-03] - 2021-08-03

### Added

- Platzhalter `[confetti: ...]` implementiert, mit sich ein Partikelregen (Konfetti) einsetzen lässt. Diese Funktion ist speziell in Kapitel nach einer Quest oder bei Erreichen des letzten Kapitels vorgesehen.

### Fixed

- Bei der Funktion `playare` wurde ein Bug bei der Angabe der Rotation gefixt, der dazu führte, dass alle Elemente an Zufallsangaben rotiert wurden. Die Angabe der Rotation wird nun respektiert.

## [201-07-30] - 2021-07-30

### Added

- Platzhalter `[fetch: ...]` implementiert, mit der ein Link in den Text gesetzt werden kann. Bei Klick auf den Link werden alle angemeldeten/registrierten Teammitglieder in das Kapitel geholt, in dem sich der aufrufende Spielende befindet. 

## [201-07-29] - 2021-07-29

### Added

- Variable `weekday` implementiert - Anzeige des deutschen Wochentags
- Variable `day` implementiert - Anzeige des aktuellen Tags als Zahl
- Variable `month` implementiert - Anzeige des aktuellen Monats als Zahl
- Variable `year` implementiert - Anzeige des aktuellen Jahrs als Zahl

### Changed

- Variablen können un mit der Zeichenfolge `%%%...%%%` angegeben werden. Dies hat den Hintergrund, dass Variablen nun auch als Beschriftung für Schaltflächen in zum Beispiel #junctions genutzt werden können. Um die Komplexität von verschachtelten Angaben mit {...} zu vermeiden, wurde das neue Format ergänzend eingefügt. Dieses sollte ab sofort in allen Angaben verwendet werden. Bestehende Definitionen können erhalten bleiben.
- In Kapitel mit #junctions werden nun inaktive Schaltflächen deutlicher (btn-outline-light) als inaktiv dargestellt.

## [201-07-27] - 2021-07-27

### Added

- Die Funktion ´Team zu mir holen´ wurde eine Möglichkeit für Teams geschaffen, mit der alle Teammitglieder zu dem Kapitel, in dem sich das aufrufenden Teammitglied befindet, delegiert werden können.

## [201-07-26] - 2021-07-26

### Fixed

- Verhalten der Lobby wurde optimiert, so dass Änderungen der registrierten Teilnehmenden schneller erkannt werden. Verwaiste Sessions werden verzögert erkannt, so dass temporäre Verzögerungen oder schlechte Verbindungsleitungen der Teilnehmer ausgeglichen werden können.

## [201-07-23] - 2021-07-23

### Changed

- Änderung der Darstellung des Changelogs: es werden nun `Markdown-Attribute mit ihrer HTML-Visualisierung` dargestellt.

## [201-07-22] - 2021-07-22

### Added

- Es wurde ein `Lobby-Modus` integriert, der nach der Registrierung alle angemeldeten Benutzer in einem Wartebereich hält. Erst wenn ein berechtigter Nutzer das erste Kapitel für die wartenden Spielenden freigibt, verlassen diese den Wartebereich automatisch und gemeinsam.

## [201-07-20] - 2021-07-20

### Added

- Für Kapitel mit Rätseln, die keine Hinweise aufweisen, wird der Tipp-Bereich in der Website nun nicht mehr angezeigt. Damit werden dem Anwender keine unnötigen oder nicht-funktionalen Bereichen auf der Website angezeigt. 
- Aufbau eines "Rätsels" `handout001-de`, bei dem eine Bestätigung durch Eingabe von `ja` oder `yes` durch den Benutzer die Kenntnis über das bereitgestellte Handout abgefragt werden kann.
- Die Funktion `feedback` wurde integriert, mit der in den Text eines Kapitels eine Umfrage eingebettet werden kann. Diese Funktion empfiehlt sich für Kapitel ohne Quest und ohne nachfolgendes Kapitel. Es können So am Ende eines Spiels Rückmeldungen von den Spielern abgefragt werden.

### Changed

- Alle bisherigen Rätsel-Definitionen wurden auf das neue Format umgestellt, bei dem Inhalte für die Darstellung dynamisch aus dem `content` Bereich der JSON gelesen werden. Dadurch können spätere Strukturänderungen an der JSON leichter umgesetzt werden.


## [201-07-14] - 2021-07-14

### Added

- Die Funktion `voice` wurde integriert. Damit können innerhalb der geschichte (Story) Sprachausgaben über den Browser in die Geschichte integriert werden. So ist es möglich, den Inhalt für Menschen mit Sehbeeinträchtigungen zugänglich zu machen oder eine umfangreichere Geschichte den Spielenden verbal verkürzt zu beschreiben.

### Changed

- Anpassung der Story CBH2021, so dass alle Kapitel nun die `voice` Funktion nutzen. Die Umsetzung wurde für das stattfindende Event CBH2021-KPK umgesetzt, um Nutzer-Feedback zu dieser neuen Funktion zu erfragen. Die angepasste Story wird aktuell in den Events CBH2021 und in CHB2021-KPK genutzt


## [201-07-13] - 2021-07-13

### Changed

- Anpassungen im Exit Game `Flug KLM427`: Bugfixes durch neue Schreibweise, Sundisc-Rätsel neu aufgebaut & Rechtschreibung

## [201-07-12] - 2021-07-12

### Added

- Aufbau des Schlüsselrätsels (ursprünglich für das CBH-Event entwickelt) im `Playarea`-Format umgesetzt.

## [201-07-11] - 2021-07-11

### Changed

- Die Schaltflächen 'Absenden' und 'Tipp nutzen' innerhalb eines Kapitels mit Rätsel nutzen nun zusätzlich `aussagekräftige Symbole` für die jeweilige Aktion.
- Die Eingabefelder für die Lösung nutzen nun `kein Autovervollständigen` mehr - dadurch werden im Screensharing die bisherigen Eingaben (diese und anderer) Rätsel nicht angezeigt und offenbart.

### Fixed

- Die Steuerung von Audio wurde optimiert, so dass abhängig davon, ob Audio wiedergegeben wird, das Icon korrekt dargestellt wird - dies ist durch die vom Creator steuerbare Option 'autoplay' bedingt gewesen.

## [201-07-10] - 2021-07-10

### Changed

- Anpassung der Registrierungsmaske, so dass anstatt eines Passwort-Felds der `Font 'text-security'` (https://github.com/noppa/text-security) genutzt wird. Dies hat den Vorteil, dass beim Absenden des Formulars der Browser nicht versucht ein Passwort zu sichern.

### Fixed

- Icon für Audio-Inhalte nun standardmäßig auf 'mute' eingestellt; Icon wechsel nun die Anzeige von 'mute' und 'up' korrekterweise

## [201-07-06] - 2021-07-06

### Changed

- In der Registrierungsmaske wird nun der Teamcode initial als Passfort-Feld angezeigt, so dass Eingaben z.B. im Screensharing nicht den Teamcode offenbaren und damit einen Missbrauch ermöglichen. Der Teamcode kann durch den Nutzenden optional sichtbar gemacht werden.

## [201-07-04] - 2021-07-04

### Added

- Verarbeitung von Informationen des CHANGELOG. Es werden die nach 'Keep a changelog' standardisierten Angaben verarbeitet und visualisiert.
- Aufbau eines Änderungsprotokolls in der Datei CHANGELOG.md 
- Überführung der Lab-Events/Stories/Quests nach Github

### Changed

- Anpassung des Github Templates 'event'

## [201-07-03] - 2021-07-03

### Added

- Unterstützung des Respository-Formats 'bundles'
- Aufbau des Github Templates 'event'

### Changed

- Wiedergabe von Audio-Medien anpasst, dass bei initial ausgeschalteter Wiedergabe nun ein Start der Wiedergabe ordnungsgemäß erfolgt. Zuvor wurde mit Stummschaltung gearbeitet, was dazu führte, dass die Datei nicht abgespielt wurde.

## [2021-07-02] - 2021-07-02

### Added

- Umstrukturierung der Github Repository, so das nun Events, Stories und Quests jeweils in einem eigenen Repository verwaltet werden können.
- Ermitteln der in einem Event eingebetteten Story und Quests und automatische Aktualisierung aller Bestandteile aus den jeweiligen dedizierten Repositories.

### Fixed

- Story-Inhalte angepasst

## [2021-07-01] - 2021-07-01

### Added

- Implementierung der Funktion 'Playarea' als einbindbare Medieninhalte; mit der 'Playarea' können interaktive Elemente auf Basis von `deckdeck-drr` eingebunden werden.
- Implementierung der Quest: Playarea
- Implementierung der Quest: Puzzle
