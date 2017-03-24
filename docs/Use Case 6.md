---
title: Travel Buddy - Use Case 6
date: 24.03.2017
author:
  - Raffaele Bof

documentclass: article
fontfamily: roboto
fontfamilyoptions: sfdefault
lang: de
toc: 1
colorlinks: 1
graphics: 1
geometry: 1
---
# UC 6: Anzeigen der Statistik (fully dressed)
## Primärer Akteur:
Reisende
## Stakeholders und Interessen:
 - Reisende: wollen eine Übersicht ihrer Tour sehen
## Vorbedingungen:
 - Reisender hat Tour beendet
## Erfolgsgarantie:
 - Reisende sieht eine anschauliche Übersicht ihrer Tour
## Standardablauf:
 1. Reisender hat seine personalisierte Tour beendet
 2. Reisender sieht die Statistik über seine Tour
 3. Reisender kann auf der Tour gemachte Fotos anschauen
 4. Reisender entscheidet ob er die Tourzusammenfassung auf Sozialen Medien veröffentlichen will
 5. Reisender bewertet die Tour
 6. Reisender sieht vorschläge für weitere Touren.
 7. Reisender wählt nächste Tour aus oder beendet.
## Alternativszenarien:
 I. Reisende bricht Tour vorzeitig ab
    1. Reisende bricht laufende Tour ab
    2. System fragt, ob die Tour abgebrochen, oder pausiert werden soll
    3. Reisende wählt abbrechen
    4. Reisende sieht die Statistik über seine Tour
    5. Reisende kann auf der Tour gemachte Fotos anschauen
    6. Reisende entscheidet ob er die Tourzusammenfassung auf Sozialen Medien veröffentlichen will
    7. Reisende bewertet die Tour
    8. Reisende sieht vorschläge für weitere Touren.
    9. Reisende wählt nächste Tour aus oder beendet.
 II.	Reisender pausiert Tour
    1. Reisender bricht laufende Tour ab
    2. System fragt, ob die Tour abgebrochen, oder pausiert werden soll
    3. Reisender wählt pausieren
    4. Reisender wird Statistik über bisherigen Fortschritt angezeigt
## Spezielle Anforderungen
 - Nicht abrufbare Daten (z.B. Schrittzähler) sollen nicht angezeigt werden.
 - Nicht vollständige Daten müssen entsprechend Hochgerechnet werden.
 - Daten sollen vor Anzeige kontrolliert werden
 - Daten sollen anschaulich und verständlich angezeigt werden.
 - Eine Graphische übersicht der Tour soll angezeigt werden.
## Auftrittshäufigkeit
 - Einmal pro Tour
# UC 5: Besuchen des nächsten Punktes bis zum Ende der Tour (Brief)
Der Reisende besuchten alle verbleibenden Punkte und bestätig das erreichen jedes einzelnen Punktes mit einem Foto. Sind alle Punkte erledigt erhält der Reisende eine Erfolgsmeldung.
# UC 4: Bestätigen des Abarbeiten eines Punktes und anzeigen des nächsten Punktes (Casual)
## Erfolgsszenario
Der Reisende erhält eine Bestätigung der App dass die Fotographie am richtigen Punkt gemacht wurde. Hierzu prüft der Server die mit dem Foto gespeicherten Metadaten (Koordinaten, Himmelsrichtung). Der aktuell markierte Punkt wird als «erledigt» markiert, und der nächste Punkt wird auf der Karte angezeigt.
## Erfolgszenario mit Fallback
Die Reisende verfügt über keine aktive Verbindung mit dem Internet, Sie erhält eine Meldung, dass das Foto an den Server übermittelt wird, sobald sich ihr Gerät wieder über eine aktive Internet Verbindung verfügt. Der aktuell markierte Punkt wird als «erledigt» markiert, und der nächste Punkt wird auf der Karte angezeigt.
