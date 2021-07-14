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

## [201-07-13] - 2021-07-12

### Changed

- Anpassungen im Exit Game Flug KLM427:
  - Bugfixes durch neue Schreibweise
  - Sundisc-Rätsel neu aufgebaut 
  - Rechtschreibung

## [201-07-12] - 2021-07-12

### Added

- Aufbau des Schlüsselrätsels (ursprünglich für das CBH-Event entwickelt) im Playarea-Format umgesetzt.

## [201-07-11] - 2021-07-11

### Changed

- Die Schaltflächen 'Absenden' und 'Tipp nutzen' innerhalb eines Kapitels mit Rätsel nutzen nun zusätzlich sprechende Symbole für die jeweilige Aktion.
- Die Eingabefelder für die Lösung nutzen nun kein Autocomplete mehr - dadurch werden im Screensharing die bisherigen Eingaben (diese und anderer) Rätsel nicht angezeigt und offenbart.

### Fixed

- Die Steuerung von Audio wurde optimiert, so dass abhängig davon, ob Audio wiedergegeben wird, das Icon korrekt dargestellt wird - dies ist durch die vom Creator steuerbare Option 'autoplay'bedingt gewesen. 

## [201-07-10] - 2021-07-10

### Changed

- Anpassung der Registrierungsmaske, so dass anstatt eines Passwort-Felds der Font 'text-security' (https://github.com/noppa/text-security) genutzt wird. Dies hat den Vorteil, dass beim Absenden des Formulars der Browser nicht versucht ein Passwort zu sichern.

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
