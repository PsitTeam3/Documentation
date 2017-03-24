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

| ID | Anwendungsfall                                                                                        | Art des Artefakts |
|----|-------------------------------------------------------------------------------------------------------|-------------------|
|  2 | User bekommt Bestätigung für das Abarbeiten des Punktes, die Route zum nächsten Punkt wird angezeigt. | brief             |
|  3 | User macht Foto am Besichtigungspunkt.                                                                | casual            |
|  4 | User läuft Route ab und sieht seine aktuellen Standort auf einer Karte.                               | fully dressed     |


# UC 4: User macht Foto am Besichtigungspunkt (brief)

Der User kommt an einem Zwischenziel z.B. einem Wahrzeichen an. Es wird nicht mehr die Karte mit der aktuellen Route angezeigt, denn der User bekommt die Moeglichkeit ueber einen Button ein Foto auszuloesen. Die App akezptiert das Foto aufgrund von Metadaten (Koordinaten, Himmelsrichtung) und zeigt wieder die Karte an. Das Zwischenziel wird als _erledigt_ markiert und die App zeigt die Route zum naechsten Zwischenziel an.

# UC 3: User läuft Route ab und sieht seinen aktuellen Standort auf einer Karte (casual)

##  Erfolgszenario 
Der User befindet sich im Freien zwischen zwei Punkte auf einer Route, also einer Teilstrecke der Tour. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an. Der User verlaesst die Route, der Marker zeigt in Echtzeit die Position an, an der er sich befindet. Die App berechnet die neue Route mit der aktuellen Postion als Ausgangslage. Der User kann also zu jederzeit die optimale Route zwischen seiner aktuellen Position und dem Ziel nachschauen.

## Erfolgszenario mit Fallback 
Der User befindet sich auf einer Tour durch eine Altstadt. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an, der Marker bewegt sich mit dem User mit. Die aktuelle Route zum nächsten Zwischenziel führt durch ein dicht überdachtes Gebiet. Die App kann die Position des Users nicht per GPS abfragen, in der Nähe stehen einige Läden und Restaurants mit WLAN. Die App kann durch eine Kombination von Standorten von Mobilfunkmasten und WLAN Sendern die aktuelle Position berechnen. Der Benutzer hat kein GPS Signal, aber sieht sich trotzdem als Punkt auf der Karte in Echtzeit.

# UC 2: User bekommt Bestätigung beim Abarbeiten der Route, der nächste Punkt wird angezeigt (fully dressed)

## Primär-Akteur
Der User (Tourist)

## Stakeholder und Interessen
* User: Will in Echtzeit Bestätigung des Fotos und die Route zum nächsten Punkt einsehen, eine sichere und möglichst interessante Route
* Touristenbüro: Will Daten zur Routenoptimierung sammeln, will User (Tourist) an sich binden und zukünftig Reisen verkaufen
* Lokale Geschäfte: Restaurants, Bars, Malls, Attraktionen (POIs) wollen möglichst viel Konsum des Touristen auf der Route
* Firma (TravelBuddy): Will aktive Teilnahme der Touristen an Bewertung der lokalen Geschäfte, will Daten zur Optimierung der App sammeln

## Vorbedingungen
* Der User (Tourist) hat die App vor Antreten der Reise auf sein Smartphone heruntergeladen. Die Mobilfunkabdeckung ist im Minimalfall vorhanden. Im Optimalfall ist die Netzabdeckung von 4G+ lückenlos und das GPS Signal auf der ganzen Route stark. 

## Erfolgsgarantie
Das Foto wurde erfolgreich vom Server validiert, die angezeigte Route ist die optimale (schnell, sicher und interessant) Strecke zwischen dem aktuellen Standort und dem nächsten Zwischenziel. 

## Standardablauf
1. Die App akzeptiert das Foto: es handelt sich um das Zwischenziel.
2. Der User will die Tour weiterführen, da er das nächste Zischenziel abhaken will. Er macht seine Position anhand der Karte aus. 
3. Die App zeigt den aktuellen Standort der Abfrage von Satellit in Echtzeit an.
4. Die App berechnet die optimale Route zum nächsten Zwischenziel.
5. Der User akzeptiert diese Route und läuft dieser entlang.

## Erweiterungen (alternative Szenarien)
### Ablauf a
1a. Die App verwirft das Foto: das Fotosubjekt wird nicht als Zwischenziel erkannt 
2a. Der User fotografiert das Zwischenziel erneut
1.  Die App akzeptiert das Foto: es handelt sich um das Zwischenziel.

### Ablauf b
2b. Der User will die Tour abbrechen und sich spontan in einem Hotel einquartieren: Er beendet die App.

### Ablauf c
3c. Die App zeigt den aktuellen Standort annähernd an. Dem User ist ersichtlich, dass es sich hierbei nur um eine Annäherung handelt.
4c. Die App berechnet die optimale Route zum nächsten Zwischenziel vom ungefähren Standort aus.
5c. Der User akezptiert die Route und läuft dieser entlang.
6c. Die App erhält Positiondaten aus mehreren Quellen, die durch die neue Position verfügbar werden.
7c. Die App korrigiert die aktuelle Position und die Route.

### Ablauf d
5d. Der User akzeptiert die Route nicht, da er einen besseren Weg kennt.
6d. Der User kommt von der Route ab, der er seinen eigenen Weg geht.
7d. Die App berechnet in Echtzeit die optimale Route der aktuellen Position zum Zwischenziel.

## Spezielle Anforderungen
* der User muss Informationen auch bei hellem Sonnenschein (z.B. in Wüstenstaat) erhalten
* der User muss Informationen auch bei sehr lauter Umgebung (z.B. Grossstadt) erhalten
* das Foto muss innerhalb von 5 Sekunden bearbeitet (also entweder akzeptiert oder verworfen) werden
* auch bei unzuverlässigem GPS Signal soll die Position des User ausreichend genau bestimmt werden
* die Route zum nächsten Punkt muss sicher sein 

## Abweichungen an Technologien
3. Das Smartphone muss nicht zwingendermassen einen GPS Chip haben.

## Offene Punkte
* Welche Quellen können mit welcher Genaugkeit zur Ortung des Users angezapft werden?
* In welchem Intervall wird die Position bestimmt? Wie verhält sich der Stromverbrauch in deren Abhängigkeit?

# Anwendungsfalldiagramm

![Anwendungsfalldiagramm](docs/diagrams/UC_Diagram_2-4.png)

# System Sequenz Diagramm
![Systemsequenzdiagramm](docs/diagrams/Sequence_Diagram_2-4.png)

# Domänenmodell
