---
title: Praktikum Anforderungen
date: 14.03.2017
author:
  - Josef Erben 

documentclass: article
fontfamily: roboto
fontfamilyoptions: sfdefault
lang: de
toc: 1
colorlinks: 1
graphics: 1
geometry: 1
---

| ID | Anwendungsfall                                                                                           | Art des Artefakts |
|----|----------------------------------------------------------------------------------------------------------|-------------------|
|  2 | Tourist bekommt Bestätigung für das Abarbeiten des Punktes, die Route zum nächsten Punkt wird angezeigt. | brief             |
|  3 | Tourist macht Foto am Besichtigungspunkt.                                                                | casual            |
|  4 | Tourist läuft Route ab und sieht seinen aktuellen Standort auf einer Karte.                             | fully dressed     |


# UC 4: Tourist macht Foto am Besichtigungspunkt (brief)

Der Tourist kommt an einem Zwischenziel z.B. einem Wahrzeichen an. Es wird nicht mehr die Karte mit der aktuellen Route angezeigt, denn der User bekommt die Möglichkeit über einen Button ein Foto auszulösen. Die App akezptiert das Foto aufgrund von Metadaten (Koordinaten, Himmelsrichtung) und zeigt wieder die Karte an. Das Zwischenziel wird als _erledigt_ markiert und die App zeigt die Route zum nächsten Zwischenziel an.

# UC 3: Tourist läuft Route ab und sieht seinen aktuellen Standort auf einer Karte (casual)

##  Erfolgsszenario 
Der Tourist befindet sich im Freien zwischen zwei Punkten auf einer Route, also einer Teilstrecke der Tour. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an. Der User verlässt die Route, der Marker zeigt in Echtzeit die Position an, an der er sich befindet. Die App berechnet die neue Route mit der aktuellen Postion als Ausgangslage. Der User kann also zu jederzeit die optimale Route zwischen seiner aktuellen Position und dem Ziel nachschauen.

## Erfolgsszenario mit Fallback 
Der Tourist befindet sich auf einer Tour durch eine Altstadt. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an, der Marker bewegt sich mit dem User mit. Die aktuelle Route zum nächsten Zwischenziel führt durch ein dicht überdachtes Gebiet. Die App kann die Position des Users nicht per GPS abfragen, in der Nähe stehen einige Läden und Restaurants mit WLAN. Die App kann durch eine Kombination von Standorten von Mobilfunkmasten und WLAN Sendern die aktuelle Position berechnen. Der Benutzer hat kein GPS Signal, aber sieht sich trotzdem als Punkt auf der Karte in Echtzeit.

# UC 2: Tourist bekommt Bestätigung beim Abarbeiten der Route, der nächste Punkt wird angezeigt (fully dressed)

## Primär-Akteur
Der Tourist

## Stakeholder und Interessen
* Tourist: Will in Echtzeit Bestätigung des Fotos und die Route zum nächsten Punkt einsehen, er will eine sichere und möglichst interessante Route
* Touristenbüro: Will Daten zur Routenoptimierung sammeln, will Tourist an sich binden und zukünftig Reisen verkaufen
* Lokale Geschäfte: Restaurants, Bars, Malls, Attraktionen (POIs) wollen möglichst viel Konsum des Touristen auf der Route
* Firma (TravelBuddy): Will aktive Teilnahme der Touristen an Bewertung der lokalen Geschäfte, will Daten zur Optimierung der App sammeln

## Vorbedingungen
* Der Tourist hat die App vor Antreten der Reise auf sein Smartphone heruntergeladen. Die Mobilfunkabdeckung ist im Minimalfall vorhanden. Im Optimalfall ist die Netzabdeckung von 4G+ lückenlos und das GPS Signal auf der ganzen Tour stark. 

## Erfolgsgarantie
Das Foto wurde erfolgreich vom Server validiert, die angezeigte Route ist die optimale (schnell, sicher und interessant) Strecke zwischen dem aktuellen Standort und dem nächsten Zwischenziel. 

## Standardablauf
1. Die App akzeptiert das Foto: Es handelt sich um das Zwischenziel.
2. Der Tourist will die Tour weiterführen, da er das nächste Zischenziel abhaken will. Er macht seine Position anhand der Karte aus. 
3. Die App zeigt den aktuellen Standort der Abfrage von Satellit in Echtzeit an.
4. Die App berechnet die optimale Route zum nächsten Zwischenziel.
5. Der Tourist akzeptiert diese Route und läuft dieser entlang.

## Erweiterungen (alternative Szenarien)
### Ablauf A 
1. Die App verwirft das Foto: Das Fotosubjekt wird nicht als Zwischenziel erkannt.
2. Der Tourist fotografiert das Zwischenziel erneut.

### Ablauf B
2. Der Tourist will die Tour abbrechen und sich spontan in einem Hotel einquartieren: Er beendet die App.

### Ablauf C
3. Die App zeigt den aktuellen Standort annähernd an. Dem Tourist ist ersichtlich, dass es sich hierbei nur um eine Näherung handelt.
4. Die App berechnet die optimale Route zum nächsten Zwischenziel vom ungefähren Standort aus.
5. Der Tourist akzeptiert die Route und läuft dieser entlang.
6. Die App erhält Positionsdaten aus mehreren Quellen, die durch die neue Position verfügbar werden.
7. Die App korrigiert die aktuelle Position und die Route.

### Ablauf D
5. Der Tourist akzeptiert die Route nicht, da er einen besseren Weg kennt.
6. Der Tourist kommt von der Route ab, da er seinen eigenen Weg geht.
7. Die App berechnet in Echtzeit die optimale Route der aktuellen Position zum Zwischenziel.

## Spezielle Anforderungen
* der Tourist muss Informationen auch bei hellem Sonnenschein (z.B. in Wüstenstaat) erhalten
* der Tourist muss Informationen auch bei sehr lauter Umgebung (z.B. Grossstadt) erhalten
* das Foto muss innerhalb von 5 Sekunden bearbeitet werden (also entweder akzeptiert oder verworfen)
* auch bei unzuverlässigem GPS Signal soll die Position des Tourist ausreichend genau bestimmt werden
* die Route zum nächsten Punkt muss sicher sein 

## Abweichungen an Technologien
3. Das Smartphone muss nicht zwingendermassen einen GPS Chip haben.

## Offene Punkte
* Welche Quellen können mit welcher Genaugkeit zur Ortung des Tourists angezapft werden?
* In welchem Intervall wird die Position bestimmt? Wie verhält sich der Stromverbrauch in deren Abhängigkeit?

# Anwendungsfalldiagramm
![Anwendungsfalldiagramm](docs/diagrams/UC_Diagram_2-4.png)

# System Sequenz Diagramm
![Systemsequenzdiagramm](docs/diagrams/Sequence_Diagram_2-4.png)

# Domänenmodell
