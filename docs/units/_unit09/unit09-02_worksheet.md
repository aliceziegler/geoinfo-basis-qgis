---
title: Lerneinheit 2 - Fragen & Antworten
toc: true
header:
  image: /assets/images/splash_L02.png
  image_description: "Post Boxes in the Marburg Area"
  caption: "Post Boxes in the Marburg Area. CC0 AG UI"
  


---


Das systematische Abfragen von Datenbankinhalten sind Sie aus dem Alltag gewöhnt. Sei es die Abfrage von Zugverbindungen, Kinokarten die Sie online bestellen  oder die Suchanfrage bei Google. <!--more-->
Auch die Integration räumlicher Attribute in Abfragen ist Alltag für Sie. Falls sie zb. die *Location based Services* in Google aktiviert haben werden Sie regelmäßig mit lokalisierter Werbung oder Abstimmungsanfragen bedacht. Doch wie können sie solche Abfragen selber gestalten und was ist die grundsätzliche Wirkungsweise?

## Was wir in dieser Einheit vor haben
In dieser Lerneinheit werden grundlegende Konzepte von Datenbankabfragen erlernt. Weniger formal werden Sie sich um die Extraktion von Daten aus Datentabellen kümmern. Abfragen in GI Systemen können sind ein wesentliches Standbein der meisten Analysen. 

## Lernziele 

Nach dieser Übung können Sie:

  *  beliebige thematische und räumliche Abfragen auf Vektordatenattribute durchführen 
  *  geometrische und topologische Abfragen unterscheiden
  *  Abfragen verknüpfen


## Benötigte Materialien

### Daten
  * [Traffic related Points of Interest](https://raw.githubusercontent.com/gisma-courses/geoinfo-basis-qgis/master/docs/assets/data/gis_osm_traffic_1.gpkg). 
  * [Wald Flächen](https://raw.githubusercontent.com/gisma-courses/geoinfo-basis-qgis/master/docs/assets/data/mr_nat.zip) Ausschnitt aus dem aktuellen Open Streetmap (OSM) Datensatz
  * [Straßen](https://raw.githubusercontent.com/gisma-courses/geoinfo-basis-qgis/master/docs/assets/data/mr_roads.zip) Ausschnitt aus dem aktuellen  Open Streetmap (OSM) Datensatz


## Aufgaben Lerneinheit 1

### Aufgabe 02-01


In der Aufgabe 02-01 werden Attributwerte abgefragt.

* Wieviel Ampeln ("traffic_signals") gibt es in Marburg?
* Wieviele Objekte weisen die Merkmalsausprägung "cafe" und "bar" auf.
* Wieviele Objekte sind weisen **nicht** die Merkmalsausprägung "university" auf?
* Wieviele Objekte beinhalten das Wort Café in ihrem Namen (Attribut name) ? 
* Welche Objekte beinhalten zwar das Wort Café in ihrem Namen, aber nicht der die Merkmalsausprägung "cafe" des Attributs flcass?
* Suchen Sie alle Objekte die den exakten Namen "REWE" haben **und** vom Typ "supermarket" sind.
* Suchen Sie alle Objekte die den exakten Namen "REWE" haben **oder** vom Typ "supermarket" sind.
{: .notice--success}


### Aufgabe 02-02


In der Aufgabe 02-02 beschäftigen wir uns mit topologischen und geometrischen Abfragen.

  - Wieviele Punkte (des POI-Datensatzes) befinden sich in Waldflächen (mr_nat)?
  - Wieviele Punkte (des POI-Datensatzes) sind maximal 150 Meter von Waldflächen entfernt?
  - Wieviele "restaurants" oder "bars"" sind max 150 Meter von Waldflächen entfernt?
  - Wieviele Straßen führen durch Waldflächen?
  - Wie viele Punkte (des POI-Datensatzes) liegen im Umkreis von 500 Metern um den Marburger Bahnhof?
  - Wie viele Bars sind maximal 500 Meter von der nächsten Bushaltestelle entfernt?
  - Wie viele Punkte (des POI-Datensatzes) liegen im Umkreis von maximal 250 Metern um Parkplätze?
  - Von wievielen Punkte (des POI-Datensatzes) aus kann ein Arzt/Krankenhaus in weniger als 500 Meter Entfernung gefunden werden?
  - Wie viele Punkte der Kategorie Gastronomie liegen weiter als 1 Kilometer vom Bahnhof und gleichzeitig weniger als 1 Kilometer vom nächsten Briefkasten entfernt?
{: .notice--success}

### Gewichtung der Aufgaben in Lerneinheit 2

| Aufgabenteil | Gewichtung Teilaufgabe | Gewichtung  Gesamt| 
|:-------------|:----------------------:|:-----------------:|
|Aufgabe 02-01 | 0.25  | 0.1  | 
|Aufgabe 02-02 | 0.75  | 0.15  | 
|**Aufgabe 02**|**1.0**| **0.25**  | 


## Hilfestellungen 

### Der Abgdrageeditor  - QGIS Dokumentation
Für die generelle Abfrage auf relational sturukturierten Datensätzen (Attributtabellen, Datenbanken) ist der [QGIS Ausdruckseditor](https://docs.qgis.org/3.22/de/docs/user_manual/expressions/expression.html) das Werkzeug der Wahl. 

### Arbeiten mit Attributen
Das nachfolgende YouTube Video macht sie in ca. 10 Minuten mit dem Umgang des Abfrageeditors vertraut. Beachten Sie auch in wie vielfältiger Weise er in QGIS zum Einsatz kommen kann.

{% include video id="eFoBztZSIaM" provider="youtube" %}


### Aufgabe 02-01

Bitte beachten Sie in jedem Fall, dass Ihre Suchbegriffe von den Datenerfasser:innen sowohl groß als auch klein, mit oder ohne Leerzeichen, nur teilweise oder auch mit oder ohne Umlaut erfasst worden sind. Auch typische Schreibfehler sind möglich.  Diese unterschiedlichen Eintragungen ein und derselben Kategorie sollten soweit es sinnvoll erscheint und möglich ist, bei den thematischen Abfragen berücksichtigt werden. 


### Aufgabe 02-02

 Sie können mehrere Abfragen hintereinander durchführen. Hierzu müssen Sie das Abfrageergebnis ggf. als neuen Layer speichern (Rechtsklick auf das selektierte Layer, dann Auswahl, dann Layer aus selektierten Features erstellen). Bitte beachten Sie, dass die so erstellten Layer nur virtuell sind. Sie können Sie aber natürlich als Geopackage-Datensatz exportieren.

