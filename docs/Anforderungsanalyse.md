---
title: Anforderungsanalyse
klass: IT15TA ZH
group: Gruppe 3
date: 28.03.2017
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
numbersections: 1
---

# Versionenlog

| **Datum**         | **Version** | **Änderung**                                         |
| ----------------  | ----------- | ---------------------------------------------------- |
| 21.03.2017        | 0.0.0       | Dokument erstellt                                    |

# Projektmanagement
TODO by Raffaele
REVIEW by Andi

# Anwendungsfälle
## UC 1: User wählt Tour aus und startet die Tour (Priorität 1)
### Primärer Akteur
Benutzer

### Stakeholders und Interessen
- Benutzer: Will mit einfachen Schritten eine passende Tour finden und starten
- Premium Tour Anbieter: Will seine Tour prominent plaziert haben um öfters ausgewählt zu werden

### Vorbedingungen
- Benutzer ist angemeldet
- Touren sind auf Server erfasst

### Erfolgsgarantie
Benutzer findete eine ansprechende Tour und kann diese starten

### Standardablauf
1. Benutzer öffnet app
2. Benutzer klickt auf neue Tour starten
3. App zeigt Auswahl von Touren
4. Benutzer öffnet Filter
5. Benutzer setzt Filter um gewünschte Tour zu finden
6. Benutzer klickt auf Tour
7. Tour wird gestartet
8. Der Benutzer begibt sich zum Startpunkt der Tour

### Erweiterungen
3a. Auswahl ist abhängig von gerade populären oder von Premium Anbietern beworbenen Touren\newline
6a. App zeigt Detailvorschau an\newline
6b. Benutzer klickt auf Tour starten oder schliessen\newline
8a. Die App zeigt dem Benutzer verschiedene Möglichkeiten an, wie er zum Startpunkt kommt.

### Spezielle Anforderungen
- Filtern der Touren muss flüssig reagieren, Resultate werden sofort angezeigt

### Auftrittshäufigkeit
Einmal pro Tour

## UC 2: User läuft Route ab und sieht seine aktuellen Standort auf einer Karte (Priorität 2)
### Erfolgszenario
Der Tourist befindet sich im Freien zwischen zwei Punkten auf einer Route, also einer Teilstrecke der Tour. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an. Der User verlässt die Route, der Marker zeigt in Echtzeit die Position an, an der er sich befindet. Die App berechnet die neue Route mit der aktuellen Postion als Ausgangslage. Der User kann also zu jederzeit die optimale Route zwischen seiner aktuellen Position und dem Ziel nachschauen.

### Erfolgszenario mit Fallback
Der Tourist befindet sich auf einer Tour durch eine Altstadt. Die App zeigt dem Benutzer seine aktuelle Position mit einem Marker (z.B. Punkt) an, der Marker bewegt sich mit dem User mit. Die aktuelle Route zum nächsten Zwischenziel führt durch ein dicht überdachtes Gebiet. Die App kann die Position des Users nicht per GPS abfragen, in der Nähe stehen einige Läden und Restaurants mit WLAN. Die App kann durch eine Kombination von Standorten von Mobilfunkmasten und WLAN Sendern die aktuelle Position berechnen. Der Benutzer hat kein GPS Signal, aber sieht sich trotzdem als Punkt auf der Karte in Echtzeit.

## UC 3: User macht Foto am Besichtigungspunkt (Priorität 2)
### Erfolgszenario
An einem Zielpunkt / Besichtigungspunkt angelangt, wird der Benutzer aufgefordert, ein Foto
von einem vorgegebenen Objekt zu erstellen. Die App entscheidet danach ob die Informationen
des Fotos mit denjenigen im System gespeicherten übereinstimmen. Stimmt das Resultat, wird
der nächste Besichtigungspunkt angezeigt.

### Alternativszenario
Befindet sich der Benutzer nicht am korrekten Ort, wird er erneut aufgefordert das
vorgegebene Objekt zu fotografieren.

## UC 4: User bekommt Bestätigung für das Abarbeiten des Punktes, die Route zum nächsten Punkt wird angezeigt. (Priorität 2)
### Erfolgszenario
Nach dem korrekten validieren der Position des Touristen, zeigt die App dem Benutzer den
nächsten Besichtigungspunkt mit einem Marker auf einer Karte an. Von seinem aktuellen Standort
wird eine vordefinierte Route zum nächsten Besichtigungspunkt abgebildet. Der Tourist
begiebt sich zum abgebildeten Punkt.

### Alternativszenario
Der Benutzer möchte die Tour unterbrechen und zu einem späteren Zeitpunkt fortsetzen. Er
schliesst die App und kehrt nach unbestimmter Zeit zurück. Die App zeigt dann den letzten
Stand und fragt nach der Weiterführung oder Abbruch der Tour.

## UC 5: User besucht nächste Punkte bis Tour zu Ende. (Priorität 2)
UC1 und UC2 werden solange wiederholt, bis der Tourist am Ende der Tour ist. Hat er den
letzten Punkt erreicht, wird dem Benutzer der Abschluss mit einer Nachricht bestätigt und
mit UC 6 fortgefahren.

## UC 6: User sieht Statistik der Tour. (Priorität 3)
Nach erfolgreichem erreichen des Zielpunktes und dem Abschluss der Tour, wird dem Benutzer
eine übersicht mit Statistiken wie z.B. der total zurück gelegten Distanz und totale
Schritte angezeigt. Durch einen klick kann der Benutzer Fotos, die Statistik und eine
Mitteilung auf den sozialen Medien teilen.

# Anwendungsfalldiagramm
TODO by Beni
REVIEW by Josef

# Domänenmodell
TODO by Nick
REVIEW by Raffaele

# Eine erste Architektur
TODO by Nick
REVIEW by Josef

# Zusätzliche Spezifikationen
TODO by Beni
REVIEW by Nick

# Systemsequenzdiagram
TODO by Andi
REVIEW by Josef

# Glossar
TODO by Raffaele
REVIEW by Beni
