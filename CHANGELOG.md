# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

- Overview of available stories
- Overview of available quests
- Online editor for events, stories and quests
- Quest ranomizer to randomized displayed quest
- User/profile management
- Wordcloud input
- Event QR codes (via permanent link)
- Sync of team players
- "Waiting points" (to ensure all players in the same position) in story

## [201-12-19] - 2021-12-19

### Improved

- Das `junction`-Handling wurde weiter verbessert, so dass die Weiterleitungen an wählbare Kapitel aber auch an das Standard-Kapitel nun durch das Frmaework geprüft werden können

## [201-12-17] - 2021-12-17

### Improved

- Die Timer-Funktionalität wurde dahingehend angepasst, dass das Ziel-Kapitel nun nicht mehr im Klartext im Code enthalten ist 

## [201-12-11] - 2021-12-11

### Added

- Die Events können nur weitere Informationen zu einem Creator aufnehmen. So können zum Beispiel Benachrichtigungen über die eigenen Events, eine Kontaktadresse für Zugangsanfragen oder die Kennzeichnung als Creator selber vorgenommen werden. Über diese Informationen kann ein Event stärker durch Creators personalisiert werden.

- Implementierung der Funktion "Teams de-/aktivieren", mit der durch einen Creator die Teamcode vor dem Event auf inaktiv gesetzt werden können, zum jeweiligen Event dann mittels Menüaufruf aktiviert werden können. So können die Zugangsdaten zuvor bekanntgegeben werden, jedoch erst zum Even selber aktiviert werden. Dies entspricht der zuvor eingeführten Funktion `Lobby` ist jedoch auf Ebene der Teams nun auch gültig für nachkommende Teammitglieder. Zudem wirkt diese Funktion (speziell bei der Deaktivierung) auch für nachträgliche Aufrufe, da damit eine Nutzung eines Events ohne aktiven Teamcode nicht mehr möglich ist.

- Fehlerhafte Anmeldeversuche werden nun mit der Ursache des Fehlers dokumentiert.

- Für Events, bei denen im `Creator`-Block eine `request`Angabe für eine E-Mail-Adresse angegeben ist, wird diese bei fehlerhaften Anmeldeversuchen gezeigt. Somit hat der Creator die Möglichkeit, die Zugänge zu dem Event eigenverantwortlich zu steuern.

- Das Feedback-Fomular am Ende eines Exit Game kann nun auch an den Creator gesendet werden. Hierzu muss der Creator in der `event.json` das Feld `feedback` im `creator`-Block setzen.

- Teams können nun über das Menü den eigenen Teamnamen anpassen. Dies gilt als Vorbereitung für eine Prüfung beim Aufruf eines Exit Games, wenn kein Name für das Team vergeben wurde und das Team zu Beginn eines Spiels den eigenen Namen vergeben muss.

### Changed

- Die neben dem Auditing erfolgende Benachrichtigung über Anmeldungen kann nun je nach Zustand (`SUCCESS` / `FAILED`) erfolgen, um so die Sicherheit des Frameworks und der Inhalte zu erhöhen.

- Die Breite der Menüs in der Oberfläche wurden verbreitert, so dass längerer Text vollständig lesbar ist.

- Benachrichtigungen zu Feedbacks werden nun anstatt mit TO mit BCC gesendet, so dass bei mehreren E-Mail-Adressen diese nicht exponiert werden.

- Repositories zu `changelog`, `features` und `benefits` werden über den Autoupdate-Mechanismus nach einer Änderung automatisch aktualisiert. 

## [201-12-10] - 2021-12-10

### Added

- in Quests können nur sowohl im `body` als auch im `solutionhint` die Variable `solution` eingesetzt werden. Somit können speziell in der Handout-Quest Hinweise zu der ersten gültigen Eingabe getätigt werden.

## [201-12-06] - 2021-12-06

### Improved

- Rätsel KLM Englische Variante weiter angepasst
 
### Improved

- Rätsel X-Mas Kontakt zum Boss angepasst und kleine Anpassungen an der Story


## [201-12-05] - 2021-12-05

### Added

- Die Median-Funktion `magnify` wurde implementiert, mit der eine Lupe auf Grafiken angezeigt werden kann, um so kleinere Elemente in Bildern sichtbar zu machen. Die Funktion arbeitet auf dem angegebenen Elemente (per ID angegeben) und unterstützt bei Mouseover über dem Element den Zoom mit einem Mausrad.

### Removed

- Die Lightbox-Funktion für Grafiken wurde auf Grund der Funktion `magnify` bis auf Weiteres deaktiviert, um auf mobilen Endgeräten keinen UX-Konflikt beim Klick von Grafiken hervorzurufen. Die Funktion wird als dediziert zu integrierende Funktion später wieder aufgenommen.

## [201-12-03] - 2021-12-03

### Added

- Die Medien-Funktion `link` wurde hinzugefügt, mit der es möglich ist, Link im generischen Format in Texte für die Story, eine Quest oder Hinweise von Quests anzugeben.

## [201-11-21] - 2021-11-21

### Added

- Der Fortschrittsbalken wird nun regelmäßig aktualisiert, so dass alle Nutzer über den aktuellen Fortschritt und Veränderungen bei den zuletzt von mindestens einem Teammitglied aufgerufenen Kapitel informiert wird. Dadurch können ohne Seiten-Aktualisierung Teammitglieder zu der jeweils aktuellen Position des Teams wechseln.

## [201-11-20] - 2021-11-20

### Improved

- Sicherheit der Anwendung weiter erhöht

## [201-11-16] - 2021-11-16

### Changed

- Teaser Quests und Story auf Public geschaltet

### Added

- Rätsel für das Teaser-Exit Game wurden erstellt und hochgeladen

## [201-11-15] - 2021-11-15

### Changed

- Die Protokollierung wurde erweitert und in die Web-Oberfläche innerhalb des Admin-Menüs integriert. Dieses Menü steht registrierten Nutzern mit der Rolle `Admin` zur Verfügung.

## [201-11-13] - 2021-11-13

### Changed

- Die Protokollierung wurde für spätere Analysen per Web-Oberfläche optimiert. 
- Das Exit Game X-Mas wurde überarbeitet

### Added 

- Neues Ende für das X-Mas Exit Game

## [201-11-03] - 2021-11-03

### Added

- Die Funktion `Schnell-Code` wurde implementiert, mit der über die Adresse https://qc.3exiteers.de und Eingabe des Codes ein Team an dem referenzierten Event angemeldet werden kann. Vorteil dieser Funktion ist, dass alle Teams mit einer identischen Startadresse das Exit Game starten können. Somit ist den Teams nicht ersichtlich, dass im Hintergrund unter Umständen unterschiedliche Exit Games gestartet werden. Zudem erleichtert dies die Kommunikation der Startadresse.

## [201-10-30] - 2021-10-30

### Fixed

- Aktualisierung der Ersetzungsfunktion für Lösungen in den Hinweisen, so dass das Kopier-Icon einen Satzbau berücksichtigt und erst nach dem Satzzeichen angezeigt wird.

## [201-10-28] - 2021-10-28

### Added

- In der Fortschrittsanzeige wird nun mit einem Positions-Symbol die aktuelle Position des Spielers in der Geschichte angezeigt. 

## [201-10-26] - 2021-10-26

### Added

- Wird über die Hinweise die Lösung angezeigt, wird neben der Lösung ein Icon zum Kopieren der Lösung in die Zwischenablage angeboten. Darüber kann der Spielende die Lösung ohne manuelle Eingabe in das Lösungsfeld einfügen. Diese Funktion ist gerade bei komplexeren Lösungen hilfreich und ermöglicht zudem ein Übertragen der Lösung in einen Team-Chat, so dass alle Nutzer die Eingabe verwenden können.

## [201-10-24] - 2021-10-24

### Added

- Die Aktualisierungen über Github wurden weiter optimiert. Repositories in der 3Exiteers Organisation rufen nun per Webhook die Aktualisierungs-Funktion auf, mit der die aktualisierten Repositories für `Event`, `Story` und `Quest` automatisch und nur für dieses Repository aktualisiert werden. Änderungen an den Repositories werden dadurch umgehend angewendet. Der bisherige Aktualisierungsmechanismus steht weiterhin zur Verfügung.

## [201-10-25] - 2021-10-23

### Added

- Neues Exit Game hinzugefügt "In der Weihnachtsfabrik"  

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

- Die Funktion `snow` wurde eingebaut, mit der herabfallende Schnellflocken zur Anzeige gebracht werden können. Als Parameter zu der Funktion kann die Anzahl der Schneeflocken angegeben werden.

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

## [201-09-06] - 2021-09-06

### Improved

- Neues Design von dem Instagram Account-Posts

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
