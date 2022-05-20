---
title: Lerneinheit 3 - Analysen
toc: true
header:
  image: /assets/images/splash_L03.png
  image_description: "SRTM ElevationModel Data Marburg"
  caption: "SRTM Elevation Model Data Marburg. CC0 AG UI"
  

---


Digitale Geländemodelle liegen in der Regel als Rasterdaten vor und werden häufig in GIS-Analysen verwendet. Dabei tragen diese sowohl unmittelbar zur Höheninformation als auch mittelbar als z. B. morphometrische oder hydrologische Basisdatensätze zum prosessorientierten Erkenntnisgewinn bei.

<!--more-->

Der Themenkomplex der digitalen Geländemodelle inkl. deren Erstellung auf Grundlage unterschiedlicher Fernerkundungssensoren ist vielfältig. Die Materialien im Reader skizzieren verschiedene häufig verwendete Ableitungen und räumliche Filter. Diese Konzepte können auf nahezu alle Rasterdaten angewendet werden.


## Was wir in dieser Einheit vor haben

Im Rahmen der Übung werden Sie Informationen aus digitalen Geländemodellen ableiten und sich mit räumlichen Filtermethoden näher beschäftigen.


## Lernziele 

Nach dieser Übung können Sie:

  *  Neue Rasterdaten durch Anwendung typischer Werkzeuge (Algorithmen) erzeugen
  *  Diese abgeleiteten Informationen in Fragestellungen zielgerichtet einsetzen
  *  Abfagen auf solchen Rasterdaten durchführen.


## Benötigte Materialien

### Daten
  * [SRTM Geländemodell CGIAR](https://srtm.csi.cgiar.org/srtmdata/) oder
  * [SRTM Geländemodell opentopography](https://portal.opentopography.org/raster?opentopoID=OTSRTM.082015.4326.1) oder
  * [SRTM Geländemodell TileDownloader Derek Watkins](https://dwtkns.com/srtm30m/) Benötigt eine Registrierung bei [NASA Earthdata](https://urs.earthdata.nasa.gov/users/new) oder
  * [SRTM OpenDEM](https://opendem.info/)
  * [Polygon Marburg Stadtgebiet]({{site.baseurl}}/assets/data/marburg_stadtgebiet.gpkg)

## Aufgaben Lerneinheit 3

## Aufgabe 03-01


* Laden Sie sich die Datenkachel für das SRTM Geländemodell von Marburg herunter.
*   Was repräsentiert der Datensatz? Schauen Sie sich die MEtadaten an. Verschaffen Sie sicheinen Überblick über die Version und Fehlerwerte.
*   Projizieren Sie das Geländemodell in ETRS89 UTM32 und schneiden es auf den Ausschnitt des Marburger Luftbildes zu.
*   Berechnen Sie die Hangneigung, Exposition/Aspect und Topographischen Index (TPI). 
*   Extrahieren Sie für den Marktplatz (Position Brunnen) die Werte aus den berechneten Datensätzen.
*   Wenden Sie einen 5*5 Mittelwertsfilter auf die Geländehöhe an.
*   Extrahieren Sie erneut für den Marktplatz (Position Brunnen) obige
Werte.
* Berechnen Sie unter Benutzung des Datensatzes ([Marburg Stadtgebiet]({{ site.baseurl}}/assets/data/marburg_stadtgebiet.gpkg)), die minimale, maximale und mittlere Hangneigung für die ausgewiesene Fläche. 

* Zeigen sie die Werte in einer Tabelle und  erläutern Sie das Resultat in einem Satz. 
{: .notice--success}

### Gewichtung der Aufgaben in Lerneinheit 3

| Aufgabenteil | Gewichtung Teilaufgabe | Gewichtung  Gesamt| 
|:-------------|:----------------------:|:-----------------:|
|**Aufgabe 03-01** | **1.0**  | **0.25** | 


## Hilfestellungen 

Alle notwendigen Informationen zu den SRTM Daten finden Sie auf der [CGIAR FAQ Seite](https://srtm.csi.cgiar.org/faq/).

Verwenden Sie zum Ausschneiden des Rasters einen der Marburg-Layer aus den vorherigen Sitzungen als Vorlage.

Das Stichwort für die QGIS Hilfe zum Mittelwertsfilter ist *"neighbors"*  oder auch *"filter"* in der Werkzeugleiste. Als Resultat wird z.B. r.neighbors aus der GRASS GIS Funktionssammlung angezeigt. bei *"filter"* gibt es eine Reihe von Treffern. Hier ist *"Simple Filter"* aus der Funktionssammlung von SAGA GIS ein guter Einstieg.

Verwenden Sie zonale Statistiken um sich die Minimum-/Maximum-/Mittel-Werte eines definierten Gebiets als Tabelle auszugeben. Für Marburg können Sie entweder ein Stadtgebiet nach ihrer Einschätzung als Polygon digitalisieren oder z.B. auf die Suche nach Verwaltungsgrenzen gehen. Hier wäre z.b. die [Bundesamt für Kartographie und Geodäsie Open Data Server](https://gdz.bkg.bund.de/index.php/default/open-data.html)  eine gute Startmöglichkeit.
 Sollte Ihnen das zu mühsam sein können  Sie auch die Datei [Marburg Stadtgebiet]({{ site.baseurl}}/assets/data/marburg_stadtgebiet.gpkg)) aus dem Download nutzen.