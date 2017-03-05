# Projektskizze #
## Ausgangslage ##
Der Tourismus ist ein schöner Zeitvertrieb und bringt viel Freude und Einblicke in andere Kulturen mit sich. In vielen Ländern existieren aber immer noch Sprachbarrieren. Dies merkt man auch bei geführten Reisetouren. Häufig spricht der Reiseführer die Sprache der Reisegruppe schlecht oder hat einen starken Akzent, so dass man seine Erläuterungen schlecht versteht. Viele Reisende sind zudem lieber autonom als mit einem Reiseführer auf einer Besichtigungstour unterwegs. Dadurch fühlt man sich freier und kann selbst entscheiden, wie lange man an einem Ort verweilen möchte. Mit Uber bietet sich auch eine flexible und kostengünstige Möglichkeit an, von einem Besichtigungspunkt zum Nächsten zu gelangen. 

## Idee ##
Wir entwickeln eine Software mit welcher Touristen auf einfache Weise verschiedene Besichtigungstouren durchführen können.
Als Reisender kann man mit der Software für seine Reise-Destinationen eine Liste von Touren zusammen stellen, welche man gerne durchführen möchte. Am jeweiligen Zielort gibt einem die Software Informationen wie man von seinem Standort an die Besichtigungspunkte gelangt und anschliessend folgen Instruktionen um an die nächsten Punkte zu gelangen. Während der Tour stellt die App auch Informationen über die Sehenswürdigkeiten bereit. Für die Wegbeschreibung wird eine Karte eingeblendet, mit welcher sich der Kunde orientieren kann und den Weg von Sehenswürdigkeit zu Sehenswürdigkeit ablaufen kann. An jedem Aufenthaltspunkt der Tour soll der Kunde ein Photo von einem bestimmten Objekt schiessen. Dieses Photo dient der App der Verifikation, dass der Kunde sich auch tatsächlich an dem vorgegebenen Besichtigungspunkt befindet. Wenn er die Tour vollständig abgelaufen hat und die App dies durch die gemachten Photos erkennt, wird ihm eine Zusammenfassungen der Tour angezeigt. Diese kann er nach Bedarf auf seinem Facebook-Profil teilen. 

Die Touren werden von anderen Firmen, wie z.B. Reisebüros erfasst. Dafür soll eine Web-Applikation entwickelt werden. Das Erfassen von Touren ist dabei kostenpflichtig. Dem Endanwender wird aber die Benutzung der Software kostenlos zur Verfügung gestellt.

## Kundennutzen ##
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

## Stand der Technik / Konkurrenzanalyse ##
Es gibt bereits andere Travelguide Apps, wie z.B. die von dem Reiseveranstalter Thomas Cook Touristik GmbH, welchem auch Neckermann Reisen gehört. Jedoch haben andere Apps nicht den gleichen Fokus auf digital geführte Reisetouren wie unsere Lösung. Die Thomas Cook Travelguide App bietet einem das Buchen von geführten Touren an und enthält auch Reiseführerinhalte.
https://play.google.com/store/apps/details?id=com.tc.android.travelguide&hl=de
Mit der App ist man jedoch an die Angebote des Reiseveranstalters gebunden. Wir wollen eine App bei denen der Anwender komplett losgelöst vom Reiseveranstalter eine Tour wählen kann. Zudem ist Uber nicht in bestehenden Apps integriert, was eine Kernfunktionalität unserer App ist, mit welcher Besichtigungstouren viel komfortabler werden. Uber stellt dazu ein API zur Verfügung, mit welchem Uber-Fahrten über fremde Apps abgewickelt werden können (auch ohne das die Uber-App selbst auf dem Gerät installiert ist). (https://developer.uber.com/products/ride-requests). Auch die Social Media Integration ist in anderen Apps nicht gegeben. Wir wollen es dem Kunden auf einfachste Weise ermöglichen, eine gemachte Tour auf Facebook zu teilen. Dabei werden Informationen über die Tour übermittelt sowie seine Photos.

## Hauptablauf ##
Hauptanwendungsfall ist der Kunde, welcher im Urlaub ist und eine Besichtigungstour in seiner aktuellen Stadt machen möchte:
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
  
## Weitere Anforderungen ##
* Das GUI Design muss einfach aber modern sein.
* Die Bedienung der App ist einfach und intuitiv.
* Der Datenverbrauch soll möglichst klein sein, so dass die App auch gut nutzbar über ein langsames Mobilfunknetz ist, oder der Kunde wenig Datenvolumen im ausländischen Mobilfunknetz verfügbar hat.
* Integration verschiedener Social Media Kanälen.
* Es sollen Voucher für die Reisenden erfasst werden können.
* Der Kunde soll die Möglichkeit haben, Touren offline durchzuführen. Dazu wählt er zu einem Zeitpunkt wo er online ist, dass er eine bestimmte Tour offline verfügbar machen möchte. In diesem Fall entfällt aber die Möglichkeit, dass der Kunde unterwegs Uber-Taxis anfordern kann.
* Beim Erfassen können die Touren kategorisiert werden (Architektur, Kultur, Sport, rollstuhlgängig, körperlich anspruchsvoll).
* Audiounterstützung für Besichtigungstouren.
* Die App kann sprachgesteuert werden.
* Alle nichtfunktionalen Anforderungen gemäss ISO Norm 25010.
