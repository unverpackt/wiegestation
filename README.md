# Wiegestation
Software und Firmware für eine Javascript und *duino basierte Wiegestation für Unverpackt-Läden bzw. Food Coops.

# Features
* Kalibrierung der Waage
* Benutzerverwaltung (Name, Foto, Kontaktdaten, [prepaid] Kontostand, ggf. Kontodaten)
* Benutzergruppen (z.B. Fördermitglieder, Aktive Mitarbeiter, Externe Nutzer, ...)
* Produktverwaltung (Name, Preis pro Benutzergruppe)
* Warenbuchungen (Eingang, Ausgang)
* Abrechnungen
* Übersicht über aktuellen Lagerbestand (auch online)
* Bestellvorschläge (wie viel, wie eilig, rückblick + prognose wie lange die gewählte Menge ausreicht)
* Kommunikation à la Facebook-Gruppe (Timeline, Statusupdate + Kommentare + Likes)
* Offlinefähig, falls kein Internet im Lager verfügbar ist
* QR-Code für Produkte und ggf. für schnellen Benutzerwechsel
* Letzter Tara Wert wird für schnellen Benutzerwechsel für jeden Benutzer separat gespeichert.
* (optional) rudimentäre Zutrittskontrolle zum Lager z.B. per QR-Code / NFC und Türsummer.

# Hardware
Küchenwaage per INA125P mit Arduino auslesen:
* http://airtripper.com/1626/arduino-load-cell-circuit-sketch-for-calibration-test/
* http://airtripper.com/1397/electronic-kitchen-scales-teardown-versus-load-cells/

Alternativ:
* http://ur5uppe.blogspot.de/2012/04/arduino-und-kuchenwaage.html
* http://gadgetmakersblog.com/hacking-kitchen-scale/

Erhöhung der Genauigkeit durch Oversampling:
* http://shelvin.de/die-aufloesung-des-adc-vom-arduino-uno-erhoehen-auf-16-bit/

#Datenhaltung und Synchronisation
Variante 1 - gerootetes Android Device mit NodeJS + MongoDB / CouchDB:
* http://www.codemonkeez.com/2014/05/how-i-got-nodejs-and-mongodb-running-on.html

Variante 2 - Apache Cordova App mit PouchDB und Synchronisation zu serverseitiger CouchDB:
* http://pouchdb.com/

