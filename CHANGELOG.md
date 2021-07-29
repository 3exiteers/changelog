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

- Variablen können un mit der Zeichenfolge `%%%...%%%` angegeben werden. Dies hat den Hintergrund, dass Variablen nun auch als Beschriftung für Schaltflächen in zum Beispiel #junctions genutzt werden können. Um die Komplexität von verschachtelten Angaben mit {...} zu vermeiden, wurde das neue Format ergänzend eingefügt. Dieses sollte ab sofort in allen Angaben verwendet werden. Betstehende Definitionen können erhalten bleiben.
- In Kapitel mit #junctions werden nun inaktive Schaltflächen deutlicher (btn-outline-light) als inaktv dargestellt.

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

- Es wurde ein `Lobby-Modus` integriert, der nach der Regsitrierung alle angemeldeten Benutzer in einem Wartebereich hält. Erst wenn ein berechtigter Nutzer das erste Kapitel für die wartenden Spielenden freigibt, verlassen diese den Wartebereich automatisch und gemeinsam.

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

- Die Steuerung von Audio wurde optimiert, so dass abhängig davon, ob Audio wiedergegeben wird, das Icon korrekt dargestellt wird - dies ist durch die vom Creator steuerbare Option 'autoplay'bedingt gewesen.

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
- Ermittelnb der in einem Event eingebetteten Story und Quests und automatische Aktualisierung aller Bestandteile aus den jeweiligen dedizierten Repositories.

### Fixed

- Story-Inhalte angepasst

## [2021-07-01] - 2021-07-01

### Added

- Implementierung der Funktion 'Playarea' als einbindbare Medieninhalte; mit der 'Playarea' können interaktive Elemente auf Basis von `deckdeck-drr` eingebunden werden.
- Implementierung der Quest: Playarea
- Implementierung der Quest: Puzzle
