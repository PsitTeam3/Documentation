---
title: Projektskizze
author:
  - Andreas Saurer
  - Benjamin Schneidinger
  - Josef Erben
  - Raffaele Bof
  - Nicolas Loth

documentclass: article
fontfamily: roboto
fontfamilyoptions: sfdefault
lang: de
toc: 1
colorlinks: 1
graphics: 1
geometry: 1
---

# Ausgangslage
Der Tourismus ist ein schöner Zeitvertrieb und bringt viel Freude und Einblicke in andere Kulturen mit sich. In vielen Ländern existieren aber immer noch Sprachbarrieren. Dies merkt man auch bei geführten Reisetouren. Häufig spricht der Reiseführer die Sprache der Reisegruppe schlecht oder hat einen starken Akzent, so dass man seine Erläuterungen schlecht versteht. Viele Reisende sind zudem lieber autonom als mit einem Reiseführer auf einer Besichtigungstour unterwegs. Dadurch fühlt man sich freier und kann selbst entscheiden, wie lange man an einem Ort verweilen möchte. Mit Uber bietet sich auch eine flexible und kostengünstige Möglichkeit an, von einem Besichtigungspunkt zum Nächsten zu gelangen.

# Idee
Wir entwickeln eine Software mit welcher Touristen auf einfache Weise verschiedene Besichtigungstouren durchführen können.
Als Reisender kann man mit der Software für seine Reise-Destinationen eine Liste von Touren zusammen stellen, welche man gerne durchführen möchte. Am jeweiligen Zielort gibt einem die Software Informationen wie man von seinem Standort an die Besichtigungspunkte gelangt und anschliessend folgen Instruktionen um an die nächsten Punkte zu gelangen. Während der Tour stellt die App auch Informationen über die Sehenswürdigkeiten bereit. Für die Wegbeschreibung wird eine Karte eingeblendet, mit welcher sich der Kunde orientieren kann und den Weg von Sehenswürdigkeit zu Sehenswürdigkeit ablaufen kann. An jedem Aufenthaltspunkt der Tour soll der Kunde ein Photo von einem bestimmten Objekt schiessen. Dieses Photo dient der App der Verifikation, dass der Kunde sich auch tatsächlich an dem vorgegebenen Besichtigungspunkt befindet. Wenn er die Tour vollständig abgelaufen hat und die App dies durch die gemachten Photos erkennt, wird ihm eine Zusammenfassungen der Tour angezeigt. Diese kann er nach Bedarf auf seinem Facebook-Profil teilen.

Die Touren werden von anderen Firmen, wie z.B. Reisebüros oder Privatbenutzern erfasst. Dafür soll eine Web-Applikation entwickelt werden. Das Erfassen von Touren ist dabei für zertifizierte Anbieter kostenpflichtig. Dem Endanwender wird aber die Benutzung der Software kostenlos zur Verfügung gestellt.

# Kundennutzen
Die Software bringt folgende Nutzen für Reisende:

* Der Reisende kann aus einem grossen Angebot von Touren diejenigen auswählen, welche am besten seine Bedürfnisse decken.
* Filterkriterien helfen dem Benutzer beim Finden von Touren.
* Der Reisende muss sich keiner Reisegruppe anschliessen und kann mit Hilfe der Software auf einfache Weise eigenständig unterwegs sein.
* Die Tour wird dem Reisenden in seiner gewünschten Sprache angezeigt.
* Dank Social Media Integration kann der Benutzer eine gemachte Tour inkl. seiner Photos mit seinen Freunden teilen.
* Die Integration von Uber bietet dem Kunden Komfort und Sicherheit. Per Knopfdruck wird innerhalb der TravelBuddy-App ein Uber-Taxi angefordert und diesem auch automatisch das Ziel bekannt gegeben. In einem Land mit hoher Kriminalitätsrate ist der Transport mit einem Uber-Taxi sicherer, als mit einem zufällig auf der Strasse angehaltenen Taxis.

Als Kunden für unsere Software zählen aber nicht nur Reisende. Auch die Anwender, welche Touren für die Software verfassen sind als Kunden zu betrachten. Dies können Reisebüros, staatliche Tourismusbüros und viele andere sein. Das Verfassen und Bereitstellen von Touren hat für Unternehmen wie Reisebüros folgende Nutzen:

* Sie sparen Kosten, da die aufwändige Organisation von Reisetouren im Ausland entfällt.
* Der Einsatz und die Unterstützung von neuen Reisemöglichkeiten wird junge, technologieversierte Leute anziehen.

# Stand der Technik / Konkurrenzanalyse
Es gibt bereits andere Travelguide Apps, wie z.B. die von dem Reiseveranstalter Thomas Cook Touristik GmbH, welchem auch Neckermann Reisen gehört. Jedoch haben andere Apps nicht den gleichen Fokus auf digital geführte Reisetouren wie unsere Lösung. Die Thomas Cook Travelguide App bietet einem das Buchen von geführten Touren an und enthält auch Reiseführerinhalte \cite{TomasCookApp}.
Mit der App ist man jedoch an die Angebote des Reiseveranstalters gebunden. Wir wollen eine App bei denen der Anwender komplett losgelöst vom Reiseveranstalter eine Tour wählen kann. Zudem ist Uber nicht in bestehenden Apps integriert, was eine Kernfunktionalität unserer App ist, mit welcher Besichtigungstouren viel komfortabler werden. Uber stellt dazu ein API zur Verfügung, mit welchem Uber-Fahrten über fremde Apps abgewickelt werden können (auch ohne das die Uber-App selbst auf dem Gerät installiert ist) \cite{UberApi}. Auch die Social Media Integration ist in anderen Apps nicht gegeben. Wir wollen es dem Kunden auf einfachste Weise ermöglichen, eine gemachte Tour auf Facebook zu teilen. Dabei werden Informationen über die Tour übermittelt sowie seine Photos gespeichert.

# Hauptablauf
Der ausführliche Hauptanwendungsfall der Grundidee  ist der Kunde, welcher im Urlaub ist und eine Besichtigungstour in seiner aktuellen Stadt machen möchte:

* Der Kunde startet die TravelBuddy-App, welche er vorgängig bereits heruntergeladen und installiert hat.
* Er sucht nach digital-geführten Reisetouren an seinem Standort.
* Er wählt die Reisetour aus, welche ihm am besten gefällt und speichert diese.
* Er betrachtet die Möglichkeiten, um an den Startpunkt der Route zu gelangen.
* Die App teilt ihm mit, wie er mit öffentlichen Verkehrsmitteln, zu Fuss oder mit Uber-Taxi an das Ziel gelangen kann.
* Der Kunde wählt die Option Uber-Taxi aus und gibt den genauen Abholort, sowie das Datum und die Uhrzeit an, an der er abgeholt werden möchte.
* Der Kunde wird zum gewählten Zeitpunkt vom Uber-Taxi abgeholt und an den Startpunkt gefahren. Die Bezahlung des Taxis wird automatisch abgewickelt.
* Die App erkennt das sich der Kunde am Startpunkt der Tour befindet und stellt ihm detaillierte Informationen über die erste Sehenswürdigkeit bereit:
  * Eine kurze Beschreibung über die Sehenswürdigkeit.
  * Eine Beschreibung, falls nötig, wie der Kunde nun definitiv ans Ziel gelangt. Z.b. "Um auf den Kirchturm zu gelangen betreten sie die Kirche durch den Sekundäreingang auf der linken Seite. Im innern der Kirche befindet sich der Turmaufgang gleich rechterhand".
* Die App fordert den Kunden auf, eine bestimmtes Objekt an dem Standort zu photographieren.
* Nachdem der Kunde den Standort fertig besichtigt hat, wählt er in der App, dass er zum nächsten Standort weiter möchte.
* Die App zeigt nun wieder die Optionen an, wie der Kunde an den nächsten Besichtigungspunkt gelangen kann (Uber-Taxi, öffentliche Verkehrsmittel, Fussmarsch).
* Der Kunde wählt den Weg zu Fuss zurückzulegen.
* Die App zeigt dem Kunden eine Karte an, welche ihn an das nächste Ziel führt.
* Hat der Kunde den letzten Punkt der Tour besichtigt, wählt er "Tour beenden" in der App.
* Die App erstellt eine persönliche Zusammenfassung seiner Tour, welche auch die von ihm gemachten Bilder enthält.
* Der Kunde wählt, dass er die zusammengefasste Tour auf seinem Facebook-Account teilen möchte.
* Die App fügt die Tour-Zusammenfassung auf seinem Account hinzu.
* Die App zeigt dem Kunden an, wie er wieder in sein Hotel zurück kommt.
* Der Kunde wählt wieder die Uber-Taxi Möglichkeit und wird kurz darauf abholt und in sein Hotel gebracht.

Aus diesem Hauptanwendungsfall leiten sich alle Teilanwendungsfälle ab. 

# Weitere Anforderungen
* Das GUI Design muss einfach und modern sein.
* Die Bedienung der App ist einfach und intuitiv.
* Der Datenverbrauch soll möglichst klein sein, so dass die App auch gut nutzbar über ein langsames Mobilfunknetz ist, oder der Kunde wenig Datenvolumen im ausländischen Mobilfunknetz verfügbar hat.
* Integration verschiedener Social Media Kanälen.
* Es sollen Voucher für die Reisenden erfasst werden können.
* Der Kunde soll die Möglichkeit haben, Touren offline durchzuführen. Dazu wählt er zu einem Zeitpunkt an dem er online ist, dass er eine bestimmte Tour offline verfügbar machen möchte. In diesem Fall entfällt aber die Möglichkeit, dass der Kunde unterwegs Uber-Taxis anfordern kann.
* Beim Erfassen können die Touren kategorisiert werden (Architektur, Kultur, Sport, rollstuhlgängig, körperlich anspruchsvoll).
* Audiounterstützung für Besichtigungstouren.
* Die App kann sprachgesteuert werden.
* Alle nichtfunktionalen Anforderungen gemäss ISO Norm 25010.

# Ressourcen
Für die Entwicklung der Anwendung werden 5 Personen benötigt. Alle müssen Erfahrung im Bereich der Objekt-Orientierten Programmierung verfügen.
Das Wissen über die Entwicklung von Mobile Apps muss angeeignet werden.
Das Team wird in zwei Gruppen aufgeteilt. Ein Backendteam bestehend aus 2 Personen sowie ein Frontendteam mit 3 Personen. Sollte eine der Gruppen in verzug kommen, bspw. durch Krankheitsausfälle, können innerhalb der Gruppen Personenressourcen geteilt oder getauscht werden.
Der Gesamtaufwand wird auf 75 Manntage geschätzt.

# Risiken
1. Da die Anwendung auf die Verwendung von Live-Kartenmaterial angewiesen ist, und dies sehr Datenintensiv sein kann, ist eine offline Verfügbarkeit der Karten wichtig, da sonst hohe Gebühren für den Endnutzer fällig werden können.
2. Das Wissen im Bereich der Entwicklung von Mobil-Apps muss zuerst angeeignet werden.
3. Der Schutz der durch die Benutzer hochgeladenen Photos gewährleistet sein.
4. Mehrere Schnittstellen und unterschiedliche Technologien bedeuten eine erhöhte Projektkomplexität.
5. Keine öffentliche und verwendbare Karten-API verfügbar.
6. Smartphone GPS Koordinaten sind zu ungenau.

# Grobplanung
Die Grobbplanung sieht die Erstellung einer ersten lauffähigen und nutzbaren Version vor. Die Entwicklungszeit wird auf 14 Wochen geschätzt. Die Entwicklung erfolgt iterativ und anwendungsfallorientiert gemäss dem Unified Process (UP). Als Iterationsdauer ist 1 Woche vorgesehen. In einer ersten Analyse wurden folgende Use-Cases und Risiken identifiziert.

## Use-Cases
1. User wählt Tour aus und startet die Tour
2. User läuft Tour ab
3. User macht Photo am Besichtigungspunkt mit bestimmter GPS-Koordinate
4. User bekommt Bestätigung, dass er an diesem Punkt war
5. User besucht nächste Punkte bis Tour zu Ende
6. User sieht Statistiken

## Grober Projektplan
Der Aufwand für das Projekt wird auf 600 Mannstunden geschätzt und in einem Zeitraum von 14 Wochen in einwöchigen Iterationen gemäss folgendem Projektplan umgesetzt.

| **Phase**          | **Iteration**    | **Start/Dauer [Wo]**   | **Ziele**                        |
| :----------------  |:---------------: | :--------------------: | :------------------------------- |
| **Inception**      | 1                | 1/2                    | Projektskizze erstellt<br /> Entwicklungsumgebung vorbereiten<br /> alle Use-Cases für erste Produktivversion definiert<br /> UI Skizze erstellt<br /> Design Guide für CI erstellt<br /> Architektur skizziert   |
| **Milestone**      | **M1**           | **Ende Woche 2**       | **Anforderung an erste Produktivversion definiert**   |
| **Elaboration**    | 2                | 3/2                    | Uses-Cases 1-3 dettailierter formuliert<br /> Entwurf des Domänenmodelles   |
|                    | 3                | 5/2                    | Uses-Cases 4-6 dettailierter formuliert<br /> Domänenmodell fertig gestellt<br />Architektur umgesetzt   |
| **Milestone**      | **M2**           | **Ende Woche 6**       | **Anforderung an erste Produktivversion verifiziert**   |
| **Construction**   | 4                | 7/2                    | Use-Case 1 und 2 realisiert und getestet<br /> UI Prototyp implementiert   |
|                    | 5                | 9/2                    | Use-Case 3 und 5 realisiert und getestet<br /> UI aktualisiert   |
|                    | 6                | 11/2                   | Use-Case 4 realisiert und getestet<br /> UI aktualisiert   |
|                    | 7                | 13/2                   | Use-Case 6 realisiert und getestet<br /> UI fertig gestellt   |
| **Milestone**      | **M3**           | **Ende Wo 14**         | Erste Produktivversion der App fertiggestellt<br /> Systemtests durchgeführt<br /> Dokumentation fertiggestellt   |       

# Wirtschaftlichkeit
Der geschätzte Aufwand beträgt 600 Mann Stunden, was etwa 3 ½ Mann Monaten entspricht, die Entwicklungskosten belaufen sich somit auf 100'000 CHF. Hinzu kommen ca. 16'000 CHF monatlich für Weiterentwicklungen und Unterhalt. Bei einem Kundenbeitrag von 2'000 CHF pro Monat für die individuelle Erstellung von Guided Tours mit Travel Buddy beläuft sich der Gewinn bei 10 Kunden auf geschätzte 4'200 CHF monatlich, zuzüglich Werbeeinahmen durch Google Ads. Somit ergibt ein return of investment nach 24 Monaten.
Durch die Flexible Erstellung von Guided Tours lässt sich eine breite Klientel, wie beispielsweise Reiseagenturen, Tourismusbüros und Gewerbeverbände, anziehen wodurch das Ziel von 10 Kunden realistisch ist.
Ideen für weitere Einnahmequellen wurden evaluiert und können zu einem späteren Zeitpunkt ausgearbeitet und implementiert werden. 

\addcontentsline{toc}{section}{Literatur}
\begin{thebibliography}{9}
\bibitem{TomasCookApp}
Thomas Cook Travelguide in Goggle Play [Online].

URL: https://play.google.com/store/apps/details?id=com.tc.android.travelguide\&hl=de [Stand: 4.3.2017].
\bibitem{UberApi}
Uber Integration für Apps [Online].

URL: https://developer.uber.com/products/ride-requests [Stand: 4.3.2017].
\end{thebibliography}
