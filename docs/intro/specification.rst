Technische Daten
================

.. image:: ../pics/Wind_Sensor_Yachta_tr.png
   :scale: 100%

Funktionen
----------

* Windspeed 0…75 kn
* Windrichtung 0…360°
* Winkelauflösung 0,1°
* Integrierter Temperatursensor -25...100 °C
* Mechanisches Funktionsprinzip
* Verschleißfreie magnetische Sensorik
* Robuste Mechanik (3 Kugellager)
* Gewicht ca. 210g
* Versorgungsspannung 7...25V / 0,36 W
* 12V Versorgung über Toplicht möglich
* Wetterfest und UV-stabil
* Keine Spezialteile aus Metall erforderlich
* Keine Kabel für Sensorsignale notwendig
* Signalübertragung per WiFi über NMEA0183
* TCP-Server Port 6666
* JSON Datenausgabe
* Aktualisierungsrate 1 Messwert pro Sekunde
* Kein Einbauinstrument notwendig
* Visualisierung auf einem  Laptop, Handy oder Tablett
* Webinterface zur Bedienung
* Passwortgeschützte Konfiguration
* Keine Extrasoftware notwendig (Web-Browser ist ausreichend)
* Firmware-Update via Internet möglich
* Datenübertragung zu AvNav, OpenCPN, SignalK, OpenPlotter und Navionics möglich
* Windsensor kann auch stationär als Wetterstation benutzt werden
* Anzeige der Winddatebn am NASA Wind Tochterdisplay


Aufbau
------

.. image:: ../pics/OBP60_Explode_View.png
   :scale: 45%


Spezifikation
-------------

+----------------------+-----------------------------+
| Versorgungsspannung  | 7...25 V                    |
+----------------------+-----------------------------+
| Stromverbrauch       | 0.36 W                      |
+----------------------+-----------------------------+
| Prozessor            | ESP8266, Single Core        |
+----------------------+-----------------------------+
| Clock Speed          | 80, 160 MHz                 |
+----------------------+-----------------------------+
| RAM                  | 160 kB                      |
+----------------------+-----------------------------+
| Flash                | 4 MB                        |
+----------------------+-----------------------------+
| Datenrate            | 1 Hz                        |
+----------------------+-----------------------------+
| NMEA0183             | WiFi, max. 50 m             |
+----------------------+-----------------------------+
| RS232-Ausgang        | 3.3 V, TTL, max. 15 m       |
+----------------------+-----------------------------+
| ESD-Schutz           | 8 kV                        |
+----------------------+-----------------------------+
| Schutzgrad           | IP68, allseitig             |
+----------------------+-----------------------------+
| Abmessungen          | 150 x 150 x 300 mm          |
+----------------------+-----------------------------+
| Gewicht              | 250 g                       |
+----------------------+-----------------------------+

Anschlussbelegung
-----------------
.. image:: ../pics/Bus_Systems.png
   :scale: 50%
   
.. image:: ../pics/Logo_ESP32-S3_t.png
   :scale: 60%
   
Schaltplan
----------

* `Schaltplan V2.1 [PDF] <../_static/files/Schematic_OBP60_V2.1.pdf>`_


Maßbilder
---------

* `Maßbild [PDF] <../_static/files/Drawing_OBP60_V2.pdf>`_

   
Nutzbare Telegramme
-------------------

**NMEA0183**
    * MWV, VWR, VPW
    
**NMEA0183 Custom**
    * INF, WST, WSE
	
Nutzbare I2C-Sensorik
---------------------

**Winkelsensoren**
	* AS5600, MT6701
	
Nutzbare 1Wire-Sensorik
-----------------------

**Temperatursensoren**
	* DS18B20
