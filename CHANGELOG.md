# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

- Overview of available stories
- Overview of available quests
- Online editor for events, stories and quests
- Quest ranomizer to randomized displayed quest
- User/profile management
- Wordcloud input
- Sync of team players
- "Waiting points" (to ensure all players in the same position) in story


## [2023-03-24] - 2023-03-24

### Fixed

- Unter besonderen Umständen wurden in Herausforderungen eingebettete Funktionen nicht korrekt dargestellt. Dadurch wurden notwendige Javascript-Bibliotheken dieser Funktionen nicht korrekt geladen und es traten Javascript-Fehle rin der Console auf. Das Problem konnte Dank eines Hinweises eines Nutzers identifiziert und korrigiert werden.


## [2023-02-05] - 2023-02-05

### Security

- Die Datei `security.txt` wurde hinzugefügt, um Hinweise zu möglichen Security-Meldungen zu ermöglichen
- Optimierte Infrastruktur, um Angriffsflächen und Risiken weiter zu reduzieren
- SPF Datensätze wurden der Domain hinzugfüht, um einen Missbrauch der Domains durch E-Mail Spoofing zu reduzieren und zu vermeiden (Kudos an den Security Researcher `Ash Day` für den Hinweis). DKIM und DMARC Datensätze folgen zeitnah. Alle Einstellungen werden nach der DNS Synchronisation sichtbar und aktiv.

## [2022-12-08] - 2022-12-08

### Added

- Die Aktion `database save` und `database load` wurden hinzugefügt, um die Variablen des Teams in der Datenbank zu speichern bzw. aus dieser zu laden. Diese Aktion ist zeitintensiver und muss daher von den Content Creators bewusst eingesetzt werden. Diese Aktionen unterstützen eine Datensicherung des aktuellen Spielfortschritts undabhängig von Event-Aktualisierungen.
- Autoupdate-Funktion um Backup-Funktion erweitert, die Verzeichnisse von `event`, `story` `quest` vor einer Aktualisierung sichert und erst nach einer Sicherung diese durch den Inhalt aktualisierter Repositories aktualisiert.

## [2022-11-16] - 2022-11-16

### Added

- Die Aktion `points` wurde hinzugefügt, um über Aktionen das Punktekonto der Teams zu verändern. Mit der Aktion können aktionsabhängige oder aktionsbasierte Veränderungen umgesetzt werden. Das Punktesystem kann somit auch zukünftig rein ´action`-basiert umgesetzt werden.
- Die Aktion `database` wurde hinzugefügt, um Variablen in die Datenbank zu schreiben oder diese aus der Datenbank zu lesen. Mit dieser Funktion können Variablen zumBeispiel bei Abschluss eines Events in der Datenbank persistiert werden. Bei Entwicklungen oder Veränderungen von Events kölnnen so die Spielfortschritte der Teams geschrieben und gelesen werden.

## [2022-11-06] - 2022-11-06

### Added

- Innerhalb der Story können nun Lösungen ergänzend oder ersetzend zu den Lösungen in der Qeust angegeben werden. Damit können von Story Creators die Eingabemöglichkeiten erweitert oder eingeschränkt werden, ohne die Quest selbst verändern zu müssen. es stehen nun die Attribute `solutions` und `expandmode` innerhalb des Bereichs `solution` zur Verfügung.
- Innerhalb der Story können nun über die Attribute `userinterface` in jedem Kapitel verschedene Elemente der Oberfläche explizit ein- und ausgeschaltet, sofern diese von dem Template unterstützt werden. Mögliche Optionen sind zum Beispiel die Beeinflussung der Anzeige von: Fortschrittsanzeige (progressbar), Hilfe (help), Hinweise (hint), Sketchpad (sketchpad) und Zusammenholen (fetch). Die Standardeinstellung ist die Anzeige, wie im Template vorgesehen.

### Improved

- Innerhalb von Lösungen können nun Variablen und dadurch dynamische Lösungen genutzt werden. So ist beispielsweise die Eingabe eines dynamisch erzeugten Teamcodes zur Verifikation oder die Abfrage einer vorherigen Eingabe, die in einer VAriable gespeichert wurde, denkbar.

## [2022-10-15] - 2022-10-15

### Improved

- Die Autoupdate-Funktion wurde um weitere Code-Verwaltungs-Dienste erweitert, so dass bei zukünftigen Erweiterungen auch alternative Verwaltungsdienste unterstützt werden. Zudem wurden die unterstützten Typen von Repositories erweitert, so dass eine flexiblere Wartung der Inhalte gegeben ist.
- Die Autoupdate-Funktion wurde als dedizierter Service umgesetzt, so dass alle Änderungen unabhängig vom Framework umgesetzt werden können. Die Services können ab sofort unabhängig gesteuert werden.


## [2022-10-10] - 2022-10-10

### Added

- Das `action` Feature `flash-notification` wurde ergänzend zu `flash` implementiert, um Spieleden nach einem Seitenwechsel nicht nur einen Dialog für eine Benachrichtigung anbieten zu können, sondern alternativ auch eine Popup-Notification, die nach wenigen Sekunden wieder ausgeblendet wird.


## [2022-10-04] - 2022-10-04

### Added

- Es wurde das Feature `action` hinzugefügt, mit dem nun aus dem Inhalt heraus angegebene Aktionen ausgeführt werden können. So können beispielweise Variablen während des Aufrufs eines Kapitels gesetzt oder zurückgesetzt werden.
 
## [2022-10-01] - 2022-10-01

### Added

- Es wurden Sub-Variablen eingeführt, die den Einstz dynamischer Inhalte in Variablen erlauben. Eine Sub-Variable kann unter anderem durch `%%%variable:var1[var2]%%%` verwendet werden.
-  Es wurden für doe Action `variable ` Aktionen zum Erhöhen oder Verringern von numerischen Variablen eingesetzt. Es stehen `inc`, `increment`, `dec`, `decrement`und `dec0` zur Verfügung. `dec0` bewirkt, dass der numerische Wert nicht unter 0 (Null) reduziert wird.

## [2022-09-29] - 2022-09-29

### Improved

- Für `responsive images` kann nun bei der Angabe des Feature-Tags `[image: ...]` der Parameter `{optimize:false}` angegeben werden, soll die Optimierung bewusst ausgeschaltet werden. Dies kann darin begründet sein, dass Dateien zwar bereitstehen, diese aber bewusst (temporär) nicht verwendet werden sollen.

## [2022-09-28] - 2022-09-28

### Added

- Es können nun weitere Auflösungen von Grafiken bereitgestellt werden, die bei kleineren Bildschirmauflösungen dem Browser angeboten werden. Es kann so das Ladeverhalten bei größeren Grafiken beeinflusst werden. Dem Dateinamen ist die Bildschirmbreite anzufügen. Stehen diese Dateien bereit, werden diese als HTML5-Tag angegeben.

## [2022-09-16] - 2022-09-16

### Improved

- Für Quests kann nun neben `solutionplaceholder` und `solutiontitle` auch neu `solutionvalue` als Inhalt (`content`) angegeben werden, so dass das Eingabefeld einen vorausgefüllten Wert anzeigt. Die Nutzung von `solutionplaceholder` hat bei angezeigten Werten dazu geführt, dass das Eingabefeld ohne Wert angesendet wurde, da die Nutzenden annehmen konnten, es sei bereits ein Wert gefüllt.

## [2022-09-15] - 2022-09-15

### Added

- Es wurde für `Quests` eine neue Funktionsweise eingeführt. Es können nur mit Angabe des Zweigs `variables` definiert werden, ob die Lösungseingabe unter einer oder mehr Variablen gespeichert werden soll. Die Eingabe ersetzt die Werte der angegebenen Variablen.

## [2022-09-14] - 2022-09-14

### Added

- Das Feature `markdown` wurde als nutzbare Funktion implementiert. Mit diesem Feature kann Inhalt im Markdown-Format eingebunden werden. Diese Funktion ist speziell für umfangreichere Texte hilfreich, wenn einfache HTML-Formatierungen genutzt werden sollen.

## [2022-09-11] - 2022-09-11

### Improved

- Javascript für Funktionen werden nun nur noch eingebunden, wenn diese Funktionen genutzt werden - so soll die Ladegeschwindigkeit am Client gesteigert werden

### Fixed

- Bei Eingabe eines falschen Teamcodes erscheintz nun wieder der Dialog zur Anfrage eines Zugangs
- Bei Absenden einer Anfrage für einen Zugang erscheint nun wieder korrekterweise eine Rückmeldung and en Nutzer, dass dei Anfrage gesendet bzw. nicht gesendet werden konnte
- Die Abfrage von Formularen mit xCaptcha wurde entfernt - es findet dadurch nun keine Nutzung eines Dritt-Service mehr statt

## [2022-04-10] - 2022-04-10

### Added

- Variable `player_uuid` implementiert

## [2022-03-17] - 2022-03-17

### Fixed

- Die Meldungen beim Zurücksetzen von Teams und deren Fortschritt wurde auf die Anzeige des Event- und Teamnamen (anstelle der IDs) umgestellt.

## [2022-03-14] - 2022-03-14

### Fixed

- Das Event Cockpit wurde korrigiert, so dass die Anzahl der absolvierten Kapitel und der Punkte pro team korrekt dargestellt werden.

## [2022-03-13] - 2022-03-13

### Improved

- Es wurden neue Variablen hinzugefügt, um während der Geschichte bereits Ergebnisse der Statistik darstellen zu können: `team_points`, `team_chapters`, `team_time`,  `team_hints` und `team_solutions`. Die genaue Beschreibung zu den Variablen ist der Dokumentation zu entnehmen.

## [2022-03-12] - 2022-03-12

### Added

- Ein Hilfesystem wurde implementiert, dass die grundlegenden Funktionen in einem Dialog-basierten Ansatz erläutert. Damit entfallen Beschreibungen innerhalb einer Story, wodurch spätere Erweiterungen nun zentral beschrieben werden können. Der Aufruf erfolgt über eine Schaltfläche unten links in jedem Kapitel einer Geschichte.

## [2022-03-05] - 2022-03-05

### Improved

- Wird in einem Spiel durch unterschiedliche Spielende unterschiedliche Pfade beschritten, gilt der erste beschrittene Pfad. Alle anderen Spielenden erhalten Die Meldung, dass dem ersten Pfad zu folgen ist. Der Hinwies wurde um einen Link zu dem Kapitel ergänzt.

## [2022-03-04] - 2022-03-04

### Fixed

- Die Statistik wurde angepasst, so dass nach der letzten Vorbereitung für eine zentrale Datenbasis die Anzeige der Spielzeiten wieder ordnungsgemäß funktioniert.
- Der Aufruf einer internen URL wurde mit einer Fehlerprüfung und Umleitung auf die Registrierungsseite angepasst, so dass dem Nutzenden eine ordnungsgemäße Anmeldung ermöglicht wird.
- Die Rätsel des Formate "Ein Rongen, um sie zu knechten" wurden angepasst, so dass ein gesteigertes Spielerlebnis ermöglicht wird.


## [2022-02-26] - 2022-02-26

### Added

- Es wurde eine Funktion implementiert, mit der Wartungs-Scripte für Datenbanken ausgeführt werden, sollte die Datenbank auf einem veralteten Stand bestehen. Dies ist hilfreich, sollte sich die Struktur der Datenbanken ändern, diese aber noch auf einem veralteten Stand bestehen.

### Fixed

- Die Berechnung des Zeitbedarfs der Herausforderungen wurde korrigiert, so dass nun die Zeiten der richtigen Kapitel berechnet werden.
- Die berechnung der Zeiten für Herausforderungen wurde mit der Funktion des Resets von Teams harmonisiert, so dass bisherige Informationen, wie zum Beuspiel Lösungseingaben, für Content Creators erhalten bleiben, jedoch nur die aktuellen Werte in die Berechnung mit einfließen.

## [2022-02-24] - 2022-02-24

### Improved

- Die Statistik für Herausforderungen wurde erweitert, so dass die Einzelbewertungen nun mehr Details zu den ergebnissen liefern.

- Die Statistik zu den Herausforderungen ermittelt nun aus allen Einzelbewertungen eine Gesamtbewertung, die für ein Event die Herausfroderungen mit den höchsten Schwierigkeitsgrad ermittelt. Diese Bewertung erfolgt anhand der benötigten Zeit, der in Anspruch genommenen Hinweis eund der erfolgten Fehleingaben für Lösungen.

### Fixed

- Die Anmedleseite für Profile wurde korrigiert, so dass eine korrekte Darstellung der Templates wieder erfolgt. Die Ursache für die damit verbundene Fehlermeldung wurde korrigiert.

## [2022-02-11] - 2022-02-11

### Added

- Die Statistik wurde im Diagramme der verschiedenen Bereiche ergänzt.

### Fixed

- Die Statistik der eingegebenen Lösungsversuche wurde korrigiert.

## [2022-02-10] - 2022-02-10

### Fixed

- Ein Fehler in der Statistik wurde korrigiert, der die Differenz der Gesamtpunkteanzahl der Teams im Vergleich zum Vorgänger falsch berechnet hat.

## [2022-02-09] - 2022-02-09

### Added

- Die Statistik wurde um eine Auswertung der benötigten Nutzungsdauern erweitert. Die Auswertung erlaubt Herausforderungen anhand der benötigten Zeiten zu bewerten.

## [2022-02-06] - 2022-02-06

### Added

- Die Statistik wurde um eine Auswertung des Rangs genutzter Hinweise erweitert. Die Auswertung erlaubt zukünftige Auswertungen für Quest-Creators, bei der herausfordernde Quests bewertet werden.  

## [2022-02-01] - 2022-02-01

### Fixed

- Die Anzeige der Spielzeiten der Kapitel wurden in der Statistik korrigiert. Die Spielzeiten werden nun korrekterweise ab dem ersten Kapitel angezeigt und die Spielzeit mit Abschluss des Spiels - dem Aufruf des letzten Kapitels - angepasst.

## [2022-01-31] - 2022-01-31

### Added

- In der Statistik werden die von den Teams benötigten Zeiten der gespielten Kapitel grafisch dargestellt. Diese Anzeige erlaubt eine schnelle Übersicht über die benötigten Spielzeiten der jeweiligen Kapitel. 

## [2022-01-29] - 2022-01-29

### Added

- In dem Event Cockpit werden nun die letzten Aktivitäten von Nutzern angezeigt, um so einen Überblick über Anmeldungen und Aktivitäten zu erhalten.
- Bereinigung temporärer Verzeichnisse optimiert.

## [2022-01-24] - 2022-01-24

### Improved

- Die Statistik zu Events wurde weiter verbessert, so dass mehr Details zu den Punkten und Zeiten verfügbar sind. Die angepassten Statistikabfragen erlauben eine schnellere Auswertung und eine Ermittlung der Differenzierungen zu anderen Teams.

## [2022-01-23] - 2022-01-23

### Improved

- Die Statistik zu Events wurde komplett dynamisiert und auf die Template-Engine umgestellt, so dass Layout-Anpassungen zukünftig einfacher vorgenommen werden können.

## [2022-01-20] - 2022-01-20

### Improved

- Das Event Cockpit wurde um eine Statistik aller Teams erweitert. Die Statistik zeigt je Team die Spielzeit, die Differenz zum Vorteam, die Differenz zum erstplatzierten Team, den Punktestand, die in Anspruch genommenen Hinweise und die Anzahl der Lösungsversuche an. 

## [2022-01-18] - 2022-01-18

### Improved

- Die Statistik wurde korrigiert, so dass die Zeitdifferenz der Übersicht nach Zeit nun krrekt berechnet und dargestellt wird.
- Die Statistik wurde korrigiert, so dass die erreichten Kapitel bei dem Team mit dem löetzten Dateneintrag nun korrekt ermittelt und dargestellt wird.
- Die Icons des Event Cockpit wurden zur besseren Lesbarkeit optimiert.

## [2022-01-17] - 2022-01-17

### Improved

- Das Event Cockpit wurde mit Funktionen zum Reset der Team-Fortschritte und der Schnell-Navigation in die Kapitel eines Events/einer Story ergänzt.

## [2022-01-16] - 2022-01-16

### Added

- Es wurde ein Event Cockpit erstellt, mit dem Content Creators eine leichtere Möglichkeit der Anpassung eines Events haben. Es können sowohl bestimmte Team-Einstellungen per Web-Obverfläche vorgenommen werde, sowie verschiedene Links zu dem Event und alle Hinweise zu dem Event bzw. der Story angezeigt werden. Dieses Cockpit bietet während der Begleitung eines Events alle notwendiogen Hinweise, die Teams optimal begleiten zu können. Außerdem kann das Cockpit zur Fehleranalyse des Events genutzt werden. 

## [2022-01-06] - 2022-01-06

### Added

- Innerhalb unserer Exit Games kann nun ein virtuelle Zeichenfläche (`3Exiteers Skratchpad`) aufgerufen werden, mit der man verschiedene Zeichenoperationen auf der Website vornehmen kann. Es sit somit möglich, dass Notizen, Verbindungen oder Markierungen vorgenommen werden können, ohne dass ein Zettel oder Stift nötig sind. Damit erreicht das 3Exiteers Framework eine neue Nutzungsqualität hin zu einer - sofern vom Anwender gewünscht - rein digitalen Form.

## [2022-01-03] - 2022-01-03

### Improved

- Das Exit Game `Die Geheimnisse von Chateau Astore` wurden für eine Veröffentlichung optimiert. 

## [2022-01-02] - 2022-01-02

### Improved

- Flash-Nachrichten werden nun über eine eigene Funktion dargestellt. Dies bietet den Vorteil, dass sowohl Titel als auch Nachricht internationalisiert werden können und damit mehr Informationen den Nutzenden dargestellt werden können.
- Flash-Nachrichten werden nun auch bei AJAX-Requests angezeigt. Die Rückmeldungen wurden entsprechend angepasst, dass eine visuell ansprechende Rückmeldung erfolgt.
- Flash-Nachrichten beinhalten nun auch eine Angabe zum zu nutzenden Style, der für das Aussehen der Rückmeldung (unter anderem Informationen, Fehler, Warnungen) genutzt wird.
- Die Anfrage nach einem Zugang zu einem Exit Game ("request for access") ist nun mit einem Captcha geschützt, so dass Anfragen von Robots verhindert werden sollten.

## [2021-12-31] - 2021-12-31

### Added

- In dem Eingabefeld für die Lösung zu einer Herausforderung wir nun ein Informations-Icon angezeigt, das bei einem Hover anzeigt, wie die Lösung vom Framework interpretiert wird und wie viele mögliche Schreibweisen der Lösung zulässig sind. Mit dieser Information können Spielende vor Eingabe erfahren, wie die Eingabe zusätzlich verändert wird, um als richtig oder falsch interpretiert zu werden.

## [2021-12-30] - 2021-12-30

### Improved

- Die Funktion Quickcode wurde erweitert, so dass der Quickcode vorausgefüllt werden kann. Dies ist hilfreich, da in der Übersicht der Exit Games nun auch eine Anzeige des für das Event gültigen Quickcode-Bestandteils erfolgt. Durch Klick auf diese Anzeige wird die Quickcode-Seite mit dem Parameter des Quickcode-Bestandteils aufgerufen.
- Mit der oben beschrieben Implementierung können nun auch vorgefertigte Links an Teilnehmer übergeben werden, bei denen nicht umgehend eine Validierung des Quickcodes erfolgt, sondern der Nutzer diesen Quickcode zuerst bestätigen muss. Diese Funktion arbeitet ergänzend zu der direkten Angabe des Quickcode als URL-Pfad-Bestandteil.
- Die Tab-Taste führt bei der Navigation innerhalb der Quickcode-Felder nun nicht mehr zum Löschen einer vorherigen EIngabe und arbeitet nun so, wie die Tasten Pfeil-links und Pfeil-rechts.
- Wird ein Quickcode vorausgefüllt, wird der Fokus der Eingabe nun auf das nächste freie Feld gesetzt. Ist der Quickcode weniger als Zeichen lang, wird der Fokus auf das vierte Feld (=das erste Feld des Teamcodes) gesetzt.
- Die Anzeige der Sprache eines Events wird nun innerhalb des Banners angezeigt. Dadurch erhalten die Tags etwas mehr Platz und bei kleineren Bildschirmen droht die Flagge nun nicht mehr unter den Button dargestellt zu werden.

## [2021-12-29] - 2021-12-29

### Improved

- Die Anmeldemaske `Quickcode` wurde optimiert und grafisch eindeutiger gestaltet. Anmeldungen mittels Quickcode setzen sich zukünftig auf drei (3) Zeichen für das Event und acht (8) Zeichen für das Team zusammen. Die Darstellung in der Quickcode-Maske unterscheidet nun auch für Creators eindeutiger zwischen diesen Bestandteilen.
- Optimierung der Template-Struktur, so dass die Templates-Derivate mit weniger individuellen Bestandteilen auskommen. Durch die Verschlankung können die Templates für Dritte deutlich leichter angepasst werden, was eine Fehleranfälligkeit reduziert.

## [2021-12-26] - 2021-12-26

### Improved

- Die Javascript-Skripte für die Fortschrittsanzeige und den Counter wurden optimiert.

## [2021-12-25] - 2021-12-25

### Added

- Für den Sync mit Github wurde der neue Typ `style` eingeführt, mit dem Stylesheets zu einer Story angegeben werden können. Mit dieser Definition ist es möglich, Styles des verwendeten Templates zu modifizieren und im Sinne der Story zu verändern. So ist es beispielsweise möglich, im Kopfbereich eines Exit Game eine Grafik anzuzeigen oder Farben für Elemente zu verändern.
- Mit der Option `storystyle` können auf Stylesheets fremder Stories verwiesen werden. Hierzu muss lediglich der Name der Story angegeben werden. - **ACHTUNG**: Diese Option referenziert, sofern vorhanden, auf eine fremde Stylesheet, die zukünftig von Dritten geändert werden kann! Damit kann nicht sichergestellt werden, dass die Styles zukünftig mit der eigenen Story kompatibel sind.

### Improved

- Das Exit Game `Flight KLM427 (deutsch)` wurde auf die neue Stylesheet-Option angepasst, so dass im Kopfbereich eine Grafik angezeigt wird.
- Das Exit Game `X-Mas v3 (deutsch)` wurde auf die neue Stylesheet-Option angepasst, so dass im Kopfbereich eine Grafik angezeigt wird.

### Changed

- Für gespielte Kapitel wurde in `junctions` der Style `btn-outline-info` aktiviert, so dass nun jeder Status eines Kapiels in einer `junction` erkennbar ist: ungespielt und deaktiviert (`btn-outline-light`), ungespielt und aktiviert (`btn-tertiary`) und gespielt und aktiviert (`btn-ountline-info`).

## [2021-12-24] - 2021-12-24

### Changed

- Die Aktion `Teams de-/aktivieren` und ´Event de-/aktvieren` geben nun Feedback an den aufrufenden Anwender. Bei der De-/Aktivierung der Teams wird nun auch aufgelistet, welche Teamcodes von der Aktion angepasst worden sind.

## [2021-12-23] - 2021-12-23

### Changed

- Die Anzeige einer Statistik ist nur für angemeldete Teams möglich, da die Teamnamen Event-spezifische sensible Informationen enthalten `können`.

### Improved

- Sollte in einem mit `timer` definierten Kapitel unterschiedliche Routen von den Teammitgliedern eingeschalten werden, gilt nur noch die zuerst eingeschlagene Route. EAs wird nur der Fortschritt und die Punkte des gültigen (ersten) Aufrufs gewertet. Davon sind die Punktevergabe und die Fortschrittsanzeige betroffen. Dadurch kann verhindert werden, dass das Team ungültige Punkteabzüge (oder -gutschriften) nicht erhält und der erste gültige Pfad verwendet wird.
- Wird ein Aufruf eines Kapitels mit `timer` von einem Teammitglied nach einer zuvor erfolgreichen Protokollierung eines anderen Pfades festgestellt, wird bei Aufruf eine Hinweismeldung diesem Teammitglied angezeigt und das Kapitel als sogenannte `deadend` dargestellt: alle Schaltflächen werden aus dem INhalt ausgeblendet und der Spielende muss über die Fortschrittsanzeige in das aktuelle Kapitel wechseln.
- Verarbeitung von Github Repositories wurde neben dem üblichen Präfixen um mögliche Suffixe erweitert, so dass die Repositories eines Exit Game nun alphabethisch zusammenhängend dargestellt werden können (bei alphabethischer Anzeige). Derzeit sind in Repository-Namen die Suffixe `.event`, `.story` und `.quest` zulässig. Die bisherigen Präfix `event-`, `story-` und `quest-` bleiben vorerst erhalten.
- Die Funktionen zum Zurücksetzen verschiedener Zustände wurde dahingehend geändert, dass nach der Rücksetzung die Registrierungsseite aufgerufen wird und die Bestätigung bzw. die Fehlermeldung als modaler Dialog angezeigt wird.

## [2021-12-19] - 2021-12-19

### Added

- Im Bereich des `junction`-Handlings wurde eine Anti-Cheat-Funktion eingebaut, die den Aufruf eines Default-Kapitels verhindert, sollten nicht alle Voraussetzungen dafür erfüllt sein.

### Improved

- Das `junction`-Handling wurde weiter verbessert, so dass die Weiterleitungen an wählbare Kapitel aber auch an das Standard-Kapitel nun durch das Framework geprüft werden können
- Die Menüstruktur für Exit Games wurde optimiert, so dass Menüeinträge in optimierter Reihenfolge angezeigt werden. Zudem werden die Einträge je nach Zustand der Anmeldung des Spielenden angezeigt.
- In der Menüstruktur ist nun der Aufruf des ersten Kapitels im angemeldeten Zustand möglich.

## [2021-12-17] - 2021-12-17

### Improved

- Die Timer-Funktionalität wurde dahingehend angepasst, dass das Ziel-Kapitel nun nicht mehr im Klartext im Code enthalten ist 

## [2021-12-11] - 2021-12-11

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

## [2021-12-10] - 2021-12-10

### Added

- in Quests können nur sowohl im `body` als auch im `solutionhint` die Variable `solution` eingesetzt werden. Somit können speziell in der Handout-Quest Hinweise zu der ersten gültigen Eingabe getätigt werden.

## [2021-12-06] - 2021-12-06

### Improved

- Rätsel KLM Englische Variante weiter angepasst
 
### Improved

- Rätsel X-Mas Kontakt zum Boss angepasst und kleine Anpassungen an der Story


## [2021-12-05] - 2021-12-05

### Added

- Die Median-Funktion `magnify` wurde implementiert, mit der eine Lupe auf Grafiken angezeigt werden kann, um so kleinere Elemente in Bildern sichtbar zu machen. Die Funktion arbeitet auf dem angegebenen Element (per ID angegeben) und unterstützt bei Mouseover über dem Element den Zoom mit einem Mausrad.

### Removed

- Die Lightbox-Funktion für Grafiken wurde auf Grund der Funktion `magnify` bis auf Weiteres deaktiviert, um auf mobilen Endgeräten keinen UX-Konflikt beim Klick von Grafiken hervorzurufen. Die Funktion wird als dediziert zu integrierende Funktion später wieder aufgenommen.

## [2021-12-03] - 2021-12-03

### Added

- Die Medien-Funktion `link` wurde hinzugefügt, mit der es möglich ist, Link im generischen Format in Texte für die Story, eine Quest oder Hinweise von Quests anzugeben.

## [2021-11-21] - 2021-11-21

### Added

- Der Fortschrittsbalken wird nun regelmäßig aktualisiert, so dass alle Nutzer über den aktuellen Fortschritt und Veränderungen bei den zuletzt von mindestens einem Teammitglied aufgerufenen Kapitel informiert wird. Dadurch können ohne Seiten-Aktualisierung Teammitglieder zu der jeweils aktuellen Position des Teams wechseln.

## [2021-11-20] - 2021-11-20

### Improved

- Sicherheit der Anwendung weiter erhöht

## [2021-11-16] - 2021-11-16

### Changed

- Teaser Quests und Story auf Public geschaltet

### Added

- Rätsel für das Teaser-Exit Game wurden erstellt und hochgeladen

## [2021-11-15] - 2021-11-15

### Changed

- Die Protokollierung wurde erweitert und in die Web-Oberfläche innerhalb des Admin-Menüs integriert. Dieses Menü steht registrierten Nutzern mit der Rolle `Admin` zur Verfügung.

## [2021-11-13] - 2021-11-13

### Changed

- Die Protokollierung wurde für spätere Analysen per Web-Oberfläche optimiert. 
- Das Exit Game X-Mas wurde überarbeitet

### Added 

- Neues Ende für das X-Mas Exit Game

## [2021-11-03] - 2021-11-03

### Added

- Die Funktion `Schnell-Code` wurde implementiert, mit der über die Adresse https://qc.3exiteers.de und Eingabe des Codes ein Team an dem referenzierten Event angemeldet werden kann. Vorteil dieser Funktion ist, dass alle Teams mit einer identischen Startadresse das Exit Game starten können. Somit ist den Teams nicht ersichtlich, dass im Hintergrund unter Umständen unterschiedliche Exit Games gestartet werden. Zudem erleichtert dies die Kommunikation der Startadresse.

## [2021-10-30] - 2021-10-30

### Fixed

- Aktualisierung der Ersetzungsfunktion für Lösungen in den Hinweisen, so dass das Kopier-Icon einen Satzbau berücksichtigt und erst nach dem Satzzeichen angezeigt wird.

## [2021-10-28] - 2021-10-28

### Added

- In der Fortschrittsanzeige wird nun mit einem Positions-Symbol die aktuelle Position des Spielers in der Geschichte angezeigt. 

## [2021-10-26] - 2021-10-26

### Added

- Wird über die Hinweise die Lösung angezeigt, wird neben der Lösung ein Icon zum Kopieren der Lösung in die Zwischenablage angeboten. Darüber kann der Spielende die Lösung ohne manuelle Eingabe in das Lösungsfeld einfügen. Diese Funktion ist gerade bei komplexeren Lösungen hilfreich und ermöglicht zudem ein Übertragen der Lösung in einen Team-Chat, so dass alle Nutzer die Eingabe verwenden können.

## [2021-10-24] - 2021-10-24

### Added

- Die Aktualisierungen über Github wurden weiter optimiert. Repositories in der 3Exiteers Organisation rufen nun per Webhook die Aktualisierungs-Funktion auf, mit der die aktualisierten Repositories für `Event`, `Story` und `Quest` automatisch und nur für dieses Repository aktualisiert werden. Änderungen an den Repositories werden dadurch umgehend angewendet. Der bisherige Aktualisierungsmechanismus steht weiterhin zur Verfügung.

## [2021-10-25] - 2021-10-23

### Added

- Neues Exit Game hinzugefügt "In der Weihnachtsfabrik"  

## [2021-10-23] - 2021-10-23

### Fixed

- Der Status der Schaltflächen in einer `#junction` wird nun für die letzte Schaltfläche der Voraussetzungen richtig gesetzt, sollten alle Voraussetzungen erfüllt sein und der Default angezeigt werden.

## [2021-10-22] - 2021-10-22

### Added

- BIG UPDATE! Wir haben auf unsere Spieler gehört! Auf vielfachen Wunsch kann nun innerhalb eines Exit Game der Fortschritt erkannt werden. Auf jeder Seite eines Exit Game wird nun die Gesamtanzahl der Kapitel als Segmente angezeigt. Mit dem Fortschritt des Teams in der Geschichte, werden die bereits vom Team erreichten Kapitel gekennzeichnet und mit einem Link versehen. Die Spieler eines Teams haben so die Möglichkeit, die bereits erreichten Kapitel durch Auswahl der Segmente direkt aufzurufen. Damit können nachfolgende Teammitglieder gleich zum letzten vom Team erreichten Kapitel springen oder das Team an ein vorheriges Kapitel zurückspringen. Wir danken allen Hinweisgebern für diese großartige Idee.

## [2021-10-19] - 2021-10-19

### Fixed

- Für Hinweis-Punkte kann nun in der `story.json` explizit für einen Hinweis `null` gesetzt werden, sollte ein Hinweis die Punkte aus der `quest.json` nutzen sollen, ein anderer jedoch nicht. Diese Option der expliziten Angabe ist als Ergänzung zu `nonsolution_hint` und `solution_hint` zu sehen.

## [2021-10-19] - 2021-10-19

### Added

- Die Funktion `snow` wurde eingebaut, mit der herabfallende Schnellflocken zur Anzeige gebracht werden können. Als Parameter zu der Funktion kann die Anzahl der Schneeflocken angegeben werden.

## [2021-10-17] - 2021-10-17

### Added

- Die Option `nonsolution_hint` in der `story.json` unterhalb der Punkteanpassungen eines Kapitels ermöglicht nun unabhängig von der Anzahl der Hinweise in einer `quest.json` die Anpassung von Punktekosten für einen normalen Hinweis. Ist die Option `solution:false` gesetzt oder diese Option nicht in der `quest.json` angegeben, überschreibt `nonsolution_hint` die Kosten für jeden normalen Hinweis dieser Quest. So können normale Hinweise unabhängig von ihrer ID (Position) mit einem - zum Beispiel - abweichenden, aber dafür identischen, Malus belegt werden. (Dank an @Fez)

- Die Option `solution_hint` in der `story.json` unterhalb der Punkteanpassungen eines Kapitels ermöglicht nun unabhängig von der Anzahl der Hinweise in einer `quest.json` die Anpassung von Punktekosten für einen finalen Hinweis. Ist die Option `solution:true` bei einem Hinweis angegeben, überschreibt `solution_hint` die Kosten für diesen Hinweis. So können auflösende Hinweise unabhängig von ihrer ID (Position) mit einem zum Beispiel höheren Malus belegt werden. (Dank an @Fez)

## [2021-10-16] - 2021-10-16

### Added

- Es können nun in der Geschichte minimale und maximale Punkte-Limits eingefügt werden. Diese Limits bewirken, dass der Punktestand der Spielenden nicht unter oder über die angegebenen Werte gezählt wird. (Dank an @Fez)

- Es kann innerhalb der Geschichte und des Events definiert werden, dass inkorrekte Lösungsversuche mit Punktabzug (Malus) berechnet werden. Diese Funktion fördert das Commitment der Spielenden eines Teams für einen Lösungsversuch. (Dank an @Fez)

## [2021-10-12] - 2021-10-12

### Added

- Social Media-Links in den Kapitel-Seiten "Registrierung" und "Abschlusskapitel"
- Feedback-Formular in der Kapitel-Seite "Abschlusskapitel"

### Improved

- Internationalisierung der Website weiter ausgebaut

## [2021-10-02] - 2021-10-02

### Added

- Die Website und das Framework wurden um Internationalisierungs-Funktionen erweitert, die eine Übersetzung der Inhalte in andere Sprachen erlauben. Der Umbau der Ausgaben auf das internationalisierbare Format wird nun sukzessive fortgeführt.

## [2021-09-18] - 2021-09-18

### Improved

- Die Analyse von fehlerhaften Seiten aufrufen wurde optimiert, um die Stabilität des Systems gewährleisten zu können.

## [2021-09-17] - 2021-09-17

### Improved

- Es wurden verschiedene statische Dateien auf dem Webserver implementiert, die eine optimierte Integration von Websiten erlauben.

## [2021-09-15] - 2021-09-15

### Added

- Die Website ermöglicht nun eine Registrierung und Anmeldung mit einem Benutzerprofil. Dadurch können in den nächsten Entwicklungen rollenbasierte Funktionen implementiert werden. Zudem wird über diese Profile zukünftig die An- und Abmeldung zum/vom Newsletter umgesetzt, so dass ein keine weitere Verifikation der E-Mailadresse erforderlich ist.
 
## [2021-09-09] - 2021-09-09

### Improved

- Die Variablen innerhalb der Inhalte (Story) werden nun zusätzlich zu den Definitionen aus den Teams und dem Event aus der Story selber ermittelt. Dabei folgt die Ersetzung der Reihenfolge `team` -> `event` -> `story`. Dieser logische Schritt ist erforderlich, um als Story Creator die eigenen Platzhalter in einer Geschichte vorgeben zu können. Event Creators können als alternative Angaben machen und sich dabei an den Variablen-Definitionen der Story orientieren.

- Die Anzeige des Dialogs für Hinweise wurde überarbeitet, um den Bereich "bisherige Tipps" beim ersten Aufruf konsistenter darzustellen, sollten noch keine Tipps in Anspruch genommen worden sein.

## [2021-09-08] - 2021-09-08

### Added

- Im Design `vfl` wurde die Hinweis-Schaltfläche `Tipps anzeigen` auf Seiten mit Herausforderungen dauerhaft im unteren rechten Bereich eingeblendet. Diese Umsetzung erfolgte auf Grund der Benutzer-Feedbacks aus dem Pilottest zum Format "Hack your way", aus dem deutlich wurde, das Hinweise unter Umständen eher in Anspruch genommen werden, wenn diese Option dem Spielenden deutlicher ist.

## [2021-09-06] - 2021-09-06

### Improved

- Neues Design von dem Instagram Account-Posts

## [2021-09-05] - 2021-09-05

### Improved

- Die Handhabung von Ausnahmesituationen (Edge cases) bei Aufruf von Events und Stories wurde verbessert und vereinheitlicht.

## [2021-09-04] - 2021-09-04

### Added

- Das Exit Game "Hackathon 2021" wurde fertig erstellt und steht die kommenden Tage für einen exklusiven Pilottest zur Verfügung.

## [2021-09-01] - 2021-09-01

### Added

- Die Variable `solution` wurde für Quests implementiert, bei der die erste angegebene Lösung aus dem Attribut `solutions` (die immer existieren muss) dynamisch ausgegeben wird. Ein Quest Creator erhält dadurch die Möglichkeit, einen abschließenden Hinweis mit ded Lösung anzugeben, ohne diese anpassen zu müssen, sollte sich die Quest beziehungsweise dessen Lösung geändert hat.

### Changed

- Hinweis vor Anzeige eines auflösenden Hinweises optimiert, so dass der Nutzende sich der weiteren Anzeige bewusst sein sollte :)

## [2021-08-29] - 2021-08-29

### Added

- Für Hinweise zu Herausforderungen wurde das Attribut `solution` (`hints` -> id -> `solution`) implementiert, mit dem ein Hinweis markiert werden kann, der die Lösung zeigt. Der Spieler wird auf diesen Umstand explizit hingewiesen.

## [2021-08-19] - 2021-08-19

### Added

- Die Funktion `handout` ermöglicht nun innerhalb der Story die Einbindung eines Deckblatts bzw. der ersten Seiten und Abschlussseiten. Zwischen diese Bestandteile werden die Handouts der Quests eingebettet, so dass bei Erzeugung ein in sich schlüssiges PDF generiert wird. 

### Changed

- Verschiedene Quests mit neuen Handouts aktualisiert
- Übertragung von Framework-Einstellungen in die App-Konfiguration
- Länge der Teamcodes auf 20 Zeichen erhöht

## [2021-08-16] - 2021-08-16

### Changed

- Updates und Änderungen an der Homeoffice Rätsel-Reihe 

## [201-08-12] - 2021-08-12

### Changed

- Update des Sundisc Rätsels, Game: Flug KLM

## [2021-08-11] - 2021-08-11

### Added

- Wir haben jetzt einen Instagram Account, besucht uns doch mal unter @3Exiteers

### Changed

- Änderungen am Exit Game Homeoffice, erstes Rätsel ersetzt und neue Funktionen eingearbeitet
- Vektorisierung der Grafik der Quest 'shiphol' 

## [2021-08-09] - 2021-08-09

### Changed

- Die Struktur sämtlicher Stories wurde auf die neue `content`-Struktur angepasst, so dass sich alle Inhalte nun aus dieser Struktur lesen lassen. Dies ist in Vorbereitung zur Umsetzung der sogenannten `branches` erfolgt, so dass alle dargestellten Inhalte einer Seite aus dieser Struktur gelesen werden.

## [2021-08-08] - 2021-08-08

### Added

- Die Website wurde um die Funktion `benefits` erweitert, auf der die Vorteile von digitalen Exit Games beschrieben werden.

### Changed

- Die Struktur und die Inhalte der Website wurden aktualisiert.

## [2021-08-07] - 2021-08-07

### Added

- Die Website wurde um den Bereich `Features` erweitert. In diesem Bereich werden die Highlights des Frameworks dargestellt und kurz beschrieben.

### Changed

- Die Navigation der Website wurde aktualisiert. Es wurden die Menüeinträge in der oberen Navigation, sowie im Fußbereich, hinsichtlich der Bezeichnung angepasst und auf die aktuellen Funktionen referenziert.

## [2021-08-03] - 2021-08-03

### Added

- Platzhalter `[confetti: ...]` implementiert, mit sich ein Partikelregen (Konfetti) einsetzen lässt. Diese Funktion ist speziell in Kapitel nach einer Quest oder bei Erreichen des letzten Kapitels vorgesehen.

### Fixed

- Bei der Funktion `playarea` wurde ein Bug bei der Angabe der Rotation gefixt, der dazu führte, dass alle Elemente an Zufallsangaben rotiert wurden. Die Angabe der Rotation wird nun respektiert.

## [2021-07-30] - 2021-07-30

### Added

- Platzhalter `[fetch: ...]` implementiert, mit der ein Link in den Text gesetzt werden kann. Bei Klick auf den Link werden alle angemeldeten/registrierten Teammitglieder in das Kapitel geholt, in dem sich der aufrufende Spielende befindet. 

## [2021-07-29] - 2021-07-29

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

## [2021-07-26] - 2021-07-26

### Fixed

- Verhalten der Lobby wurde optimiert, so dass Änderungen der registrierten Teilnehmenden schneller erkannt werden. Verwaiste Sessions werden verzögert erkannt, so dass temporäre Verzögerungen oder schlechte Verbindungsleitungen der Teilnehmer ausgeglichen werden können.

## [2021-07-23] - 2021-07-23

### Changed

- Änderung der Darstellung des Changelogs: es werden nun `Markdown-Attribute mit ihrer HTML-Visualisierung` dargestellt.

## [2021-07-22] - 2021-07-22

### Added

- Es wurde ein `Lobby-Modus` integriert, der nach der Registrierung alle angemeldeten Benutzer in einem Wartebereich hält. Erst wenn ein berechtigter Nutzer das erste Kapitel für die wartenden Spielenden freigibt, verlassen diese den Wartebereich automatisch und gemeinsam.

## [2021-07-20] - 2021-07-20

### Added

- Für Kapitel mit Rätseln, die keine Hinweise aufweisen, wird der Tipp-Bereich in der Website nun nicht mehr angezeigt. Damit werden dem Anwender keine unnötigen oder nicht-funktionalen Bereichen auf der Website angezeigt. 
- Aufbau eines "Rätsels" `handout001-de`, bei dem eine Bestätigung durch Eingabe von `ja` oder `yes` durch den Benutzer die Kenntnis über das bereitgestellte Handout abgefragt werden kann.
- Die Funktion `feedback` wurde integriert, mit der in den Text eines Kapitels eine Umfrage eingebettet werden kann. Diese Funktion empfiehlt sich für Kapitel ohne Quest und ohne nachfolgendes Kapitel. Es können So am Ende eines Spiels Rückmeldungen von den Spielern abgefragt werden.

### Changed

- Alle bisherigen Rätsel-Definitionen wurden auf das neue Format umgestellt, bei dem Inhalte für die Darstellung dynamisch aus dem `content` Bereich der JSON gelesen werden. Dadurch können spätere Strukturänderungen an der JSON leichter umgesetzt werden.


## [2021-07-14] - 2021-07-14

### Added

- Die Funktion `voice` wurde integriert. Damit können innerhalb der Geschichte (Story) Sprachausgaben über den Browser in die Geschichte integriert werden. So ist es möglich, den Inhalt für Menschen mit Sehbeeinträchtigungen zugänglich zu machen oder eine umfangreichere Geschichte den Spielenden verbal verkürzt zu beschreiben.

### Changed

- Anpassung der Story CBH2021, so dass alle Kapitel nun die `voice` Funktion nutzen. Die Umsetzung wurde für das stattfindende Event CBH2021-KPK umgesetzt, um Nutzer-Feedback zu dieser neuen Funktion zu erfragen. Die angepasste Story wird aktuell in den Events CBH2021 und in CHB2021-KPK genutzt


## [2021-07-13] - 2021-07-13

### Changed

- Anpassungen im Exit Game `Flug KLM427`: Bugfixes durch neue Schreibweise, Sundisc-Rätsel neu aufgebaut & Rechtschreibung

## [2021-07-12] - 2021-07-12

### Added

- Aufbau des Schlüsselrätsels (ursprünglich für das CBH-Event entwickelt) im `Playarea`-Format umgesetzt.

## [2021-07-11] - 2021-07-11

### Changed

- Die Schaltflächen 'Absenden' und 'Tipp nutzen' innerhalb eines Kapitels mit Rätsel nutzen nun zusätzlich `aussagekräftige Symbole` für die jeweilige Aktion.
- Die Eingabefelder für die Lösung nutzen nun `kein Autovervollständigen` mehr - dadurch werden im Screensharing die bisherigen Eingaben (diese und anderer) Rätsel nicht angezeigt und offenbart.

### Fixed

- Die Steuerung von Audio wurde optimiert, so dass abhängig davon, ob Audio wiedergegeben wird, das Icon korrekt dargestellt wird - dies ist durch die vom Creator steuerbare Option 'autoplay' bedingt gewesen.

## [2021-07-10] - 2021-07-10

### Changed

- Anpassung der Registrierungsmaske, so dass anstatt eines Passwort-Felds der `Font 'text-security'` (https://github.com/noppa/text-security) genutzt wird. Dies hat den Vorteil, dass beim Absenden des Formulars der Browser nicht versucht ein Passwort zu sichern.

### Fixed

- Icon für Audio-Inhalte nun standardmäßig auf 'mute' eingestellt; Icon wechsel nun die Anzeige von 'mute' und 'up' korrekterweise

## [2021-07-06] - 2021-07-06

### Changed

- In der Registrierungsmaske wird nun der Teamcode initial als Passfort-Feld angezeigt, so dass Eingaben z.B. im Screensharing nicht den Teamcode offenbaren und damit einen Missbrauch ermöglichen. Der Teamcode kann durch den Nutzenden optional sichtbar gemacht werden.

## [2021-07-04] - 2021-07-04

### Added

- Verarbeitung von Informationen des CHANGELOG. Es werden die nach 'Keep a changelog' standardisierten Angaben verarbeitet und visualisiert.
- Aufbau eines Änderungsprotokolls in der Datei CHANGELOG.md 
- Überführung der Lab-Events/Stories/Quests nach Github

### Changed

- Anpassung des Github Templates 'event'

## [2021-07-03] - 2021-07-03

### Added

- Unterstützung des Respository-Formats 'bundles'
- Aufbau des Github Templates 'event'

### Changed

- Wiedergabe von Audio-Medien anpasst, dass bei initial ausgeschalteter Wiedergabe nun ein Start der Wiedergabe ordnungsgemäß erfolgt. Zuvor wurde mit Stummschaltung gearbeitet, was dazu führte, dass die Datei nicht abgespielt wurde.

## [2021-07-02] - 2021-07-02

### Added

- Umstrukturierung der Github Repository, so dass nun Events, Stories und Quests jeweils in einem eigenen Repository verwaltet werden können.
- Ermitteln der in einem Event eingebetteten Story und Quests und automatische Aktualisierung aller Bestandteile aus den jeweiligen dedizierten Repositories.

### Fixed

- Story-Inhalte angepasst

## [2021-07-01] - 2021-07-01

### Added

- Implementierung der Funktion 'Playarea' als einbindbare Medieninhalte; mit der 'Playarea' können interaktive Elemente auf Basis von `deckdeck-drr` eingebunden werden.
- Implementierung der Quest: Playarea
- Implementierung der Quest: Puzzle
