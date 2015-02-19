---
---

# NT-Meter - Anleitung

## Übersicht

**TODO**: Produktbeschreibung

**TODO** Bild einfügen


## Installation

**TODO**: Leseköpfe positionieren und anschließen, Netzwerk anschließen, Stromversorgung herstellen, IP-Adresse ermitteln (Fritzbox), Oberfläche aufrufen (http://<ip des gerätes>/frontend)


## Benutzeroberfläche

**TODO**: Kanalliste, Diagrammanzeige, Tacho


## Konfiguration

**TODO**

### Kanäle anlegen und konfigurieren

**TODO**

### Emailbenachichtigung konfigurieren

**TODO**


## Datensicherung und -wiederherstellung

Zur Datensicherung und -wiederherstellung dient das Werkzeug phpmyadmin.

### Zugangsdaten

Die Zugangsdaten für phpmyadmin sind mit den Zugangsdaten für daen Raspberry Pi identisch. 

  - Username: pi
  - Passwort: raspberry

### Datensicherung

  1. phpmyadmin aufrufen

    Im Browser die folgende Adresse eingeben: http://<ip des gerätes>/phpmyadmin/index.php?db=volkszaehler
    Die Datenbank des NT Meters trägt den Namen `volkszaehler`.

    ![Sicherung vorbereiten](img/export.png?raw=true)
    
  2. Daten exportieren

    Menüpunkt `Export` auswählen. Optionen bestätigen und Export starten:
    
    ![Sicherung starten](img/export2.png?raw=true)

    Das Backup wird als .sql Datei auf dem lokalen Rechner gespeichert. Diese Datei wird auch für die Wiederherstellung der Daten bei der Rücksicherung benötigt und sollte an einem sicheren Ort aufbewahrt werden.

### Datenwiederherstellung

  1. phpmyadmin aufrufen

    Der Aufruf von phpmyadmin erfolgt analog zur Datensicherung.

  2. Daten importieren

	Menüpunkt `Import` auswählen. Sicherungsdatei auswählen und Import starten. Die Sicherung wird aus der .sql Datei auf dem lokalen Rechner wiederhergestellt:
	
	![Wiederherstellung](img/import.png?raw=true)


## Administration

Das NT-Meter basiert auf dem Raspberry Pi [http://www.raspberrypi.org/](http://www.raspberrypi.org/). Als Betriebssystem wird Raspbian verwendet [http://www.raspbian.org/](http://www.raspbian.org/).

Das System kann auf eigene Anforderungen angepasst werden. Dafür steht ein Zugang über das SSH Protokoll, Port 22, zur Verfügung:

  - Username: pi
  - Passwort: raspberry

**ACHTUNG**: Diese Möglichkeit erfordert Kenntnisse in Benutzung der Linux Kommandozeile. Unbedachte Änderungen können das NT-Meter unbrauchbar machen.

