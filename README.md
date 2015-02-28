# NT-Meter - Anleitung

**TODO** Primer

### Inhaltsverzeichnis

  10. [Übersicht](#übersicht)
  20. [Support](#support)
  20. [Datensicherung und -wiederherstellung](#datensicherung-und--wiederherstellung)


## Übersicht

**TODO**: Produktbeschreibung

**TODO** Bild einfügen


## Support

Wenn Sie Unterstützung bei der Verwendung Ihres NT-Meters benötigen nutzen Sie bitte die Funktion "Issues" um Ihre Fehlermeldungen oder Probleme im Supportforum zu melden:

https://github.com/sw-nuertingen/nt-meter/issues

### Anmeldung

Für den Zugang zum Supportforum melden Sie sich nach Eingabe der Adresse im Webbroswer bitte einmalig bei GitHub an:

![Anmeldung](img/signup.png?raw=true)

Für die Anmeldung benötigen Sie Ihre Emailadresse.


## Installation

**TODO**: Leseköpfe positionieren und anschließen, Netzwerk anschließen, Stromversorgung herstellen, IP-Adresse ermitteln (Fritzbox), Oberfläche aufrufen (http://ip.adresse.des.gerätes/frontend)


## Benutzeroberfläche

**TODO**: Kanalliste, Diagrammanzeige, Tacho


## Konfiguration

**TODO**

**Zählertypen**

**Auflösung des Ferraris Zählers konfigurieren**

### Kanäle anlegen und konfigurieren

**TODO**

### Emailbenachichtigung konfigurieren

**TODO**


## Datensicherung und -wiederherstellung

Zur Datensicherung und -wiederherstellung dient das Werkzeug *phpmyadmin*.

### Zugangsdaten

Die Zugangsdaten für *phpmyadmin* sind mit den Zugangsdaten für den Raspberry Pi identisch.

  - Username: pi
  - Passwort: raspberry

### Datensicherung

  1. phpmyadmin aufrufen

    Im Browser die folgende Adresse eingeben: http://ip.adresse.des.gerätes/phpmyadmin/index.php?db=volkszaehler
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

Die Software des NT-Meter basiert auf dem Projekt [Volkszähler](http://volkszahler.org), einer Smart Meter Plattform mit Fokus auf Datensicherschutz und Einhaltung der Privatsphäre. [Volkszähler](http://volkszahler.org) unterliegt der GNU Publi License. Die verwendeten Quelltexte und Lizenzbestimmungen sind Bestandteil des NT-Meters und können über der Adminsitrationszugang eingesehen werden.

Das System kann auf eigene Anforderungen angepasst werden. Dafür steht ein Zugang über das SSH Protokoll, Port 22, zur Verfügung:

  - Username: pi
  - Passwort: raspberry

**ACHTUNG**: Diese Möglichkeit erfordert Kenntnisse in Benutzung der Linux Kommandozeile. Unbedachte Änderungen können das NT-Meter unbrauchbar machen.
