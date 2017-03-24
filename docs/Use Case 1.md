---
title: Travel Buddy - Use Case 1
date: 14.03.2017
author:
  - Andreas Saurer

documentclass: article
fontfamily: roboto
fontfamilyoptions: sfdefault
lang: de
toc: 1
colorlinks: 1
graphics: 1
geometry: 1
---

# UC 1: User wählt Tour aus und startet die Tour (fully dressed)
## Primärer Akteur
Benutzer

## Stakeholders und Interessen
- Benutzer: Will mit einfachen Schritten eine passende Tour finden und starten
- Premium Tour Anbieter: Will seine Tour prominent plaziert haben um öfters ausgewählt zu werden

## Vorbedingungen
- Benutzer ist angemeldet
- Touren sind auf Server erfasst

## Erfolgsgarantie
Benutzer findete eine ansprechende Tour und kann diese starten

## Standardablauf
1. Benutzer öffnet app
2. Benutzer klickt auf neue Tour starten
3. App zeigt Auswahl von Touren
4. Benutzer öffnet Filter
5. Benutzer setzt Filter um gewünschte Tour zu finden
6. Benutzer klickt auf Tour
7. Tour wird gestartet
8. Der Benutzer begibt sich zum Startpunkt der Tour

## Erweiterungen
3.
  a. Auswahl ist abhängig von gerade populären oder von Premium Anbietern beworbenen Touren
6.
  a. App zeigt Detailvorschau an
  b. Benutzer klickt auf Tour starten oder schliessen
8.
  a. Die App zeigt dem Benutzer verschiedene Möglichkeiten an, wie er zum Startpunkt kommt.

## Spezielle Anforderungen
- Filtern der Touren muss flüssig reagieren, Resultate werden sofort angezeigt

## Auftrittshäufigkeit
Einmal pro Tour

# UC 2: User läuft Route ab und sieht seine aktuellen Standort auf einer Karte (casual)
## Standardablauf
Der Benutzer läuft zum angezeigten Punkt auf der Karte. Auf der Karte ist jeweils der
Standort des Benutzers und des Ziels ersichtlich.

## Erweiterungen
Dem Benutzer werden visuell Anweisungen zum optimalen erreichen des Zielortes angezeigt.
Während dem Ablaufen der Route kann der Benutzer auf Angebote von Partnern in der Nähe
aufmerksam gemacht werden.

# UC 3: User macht Foto am Besichtigungspunkt (brief)
An einem Zielpunkt / Besichtigungspunkt angelangt, wird der Benutzer aufgefordert, ein Foto
von einem vorgegebenen Objekt zu erstellen. Die App entscheidet danach ob die Informationen
des Fotos mit denjenigen im System gespeicherten übereinstimmen. Stimmt das Resultat, wird
der nächste Besichtigungspunkt angezeigt. Falls er falsch ist wird der Benutzer erneut
aufgefordert das vorgegebene Objekt zu fotografieren.

# Anwendungsfalldiagramm
![Anwendungsfalldiagramm](docs/diagrams/UC_Diagram_1-3.png)

# Systemsequenz Diagramm
![Systemsequenzdiagramm](docs/diagrams/System_Sequence_Diagram_1-3.png)

# Domänenmodell
