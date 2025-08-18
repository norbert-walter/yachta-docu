###############################
Windsensor Yachta Dokumentation
###############################
Letzte Aktualisierung |today|

.. image:: https://readthedocs.org/projects/yachta-docu/badge/?version=latest
    :target: https://yachta-docu.readthedocs.io/de/latest/?badge=latest
    :alt: Documentation Status

.. note::
   Diese Seiten sind noch in Bearbeitung.

.. image:: /pics/Screen_Overview.png
             :scale: 50%

Der Windsensor Yachta dient zur Messung der Windgeschwindigkeit und der Windrichtung auf Booten. Er wird am Mast installiert und mit 12V versorgt. Die Datenübertragung der NMEA0183 Telegramme erfolgt drahtlos per WiFi. Im Windsensor befindet sich ein Access Point und ein kleiner Webserver. Als Messwertanzeige dient ein Handy mit einen Webbrowser. Es gibt ebenfalls eine Android-App mit der die Daten angezeigt werden können. Die Messdaten lassen sich auch in anderen Programmen wie SignalK, AvNav, OpenCPN, Navionics o.ä. übertragen und angezeigen.

Der Windsensopr Yachta ist so konzipiert, dass er als DIY-Projekt nachgebaut werden kann. Alle technischen Unterlagen stehen als Open Hardware, Open Source und Open Date zur Verfügung und sind bei GitHub veröffentlicht. Für den einfachen Nachbau kann über Open Boat Projects eine bestückte, programmierte und getestete Platine erworben werden. Der Nachbau beschränkt sich dann größtenteils auf die Beschaffung von mechanischen Komponenten, die Erstellung von 3D-Teilen und den machanischen Zusammenbau. Der Windsensor Yachta wurde schon über 200 Mal erfolgreich nachgebaut und hat eine große weltweite Fangemeinde. Der Service und Support erfolgt über das Segeln-Forum in deutscher oder englischer Sprache. Dort helfen kompetente Forenmitglieder, die selber einen Windsensor Yachta zusammengebaut haben. Das Core-Entwicklerteam ist dort auch anzutreffen.

.. toctree::
   :maxdepth: 3
   :caption: Einführung
   :name: sec-intro

   Historie <intro/historie>
   Technische Daten <intro/specification>
   
.. toctree::
   :maxdepth: 3
   :caption: Bedienung
   :name: sec-usermanual

   Funktionsweise <usermanual/functionality>
   Bedienelemente <usermanual/elements>
   Inbetriebnahme <usermanual/start>
   Konfiguration <usermanual/configuration>
   Bussysteme <usermanual/bussystems>
   Datenaustausch <usermanual/dataexchange>
   Erweiterte Sensorik <usermanual/sensors>
   Beispielkonfiguration <usermanual/samples>
   Sicherheitshinweise <usermanual/safety>

.. toctree::
   :maxdepth: 3
   :caption: Zusammenbau
   :name: sec-assembling
   
   Geräteaufbau <assembling/device>
   Vorbereitung <assembling/preparation>
   Bauteilliste <assembling/partlist>
   Durchführung <assembling/actionsteps>
   Funktionstest <assembling/tests>
   
.. toctree::
   :maxdepth: 3
   :caption: Programmierung
   :name: sec-programming   

   Programmierumgebung <programming/environment>
   Seitenerstellung <programming/pages>
   Kompilieren und Download <programming/activating>
   Web-Flashtool <programming/webflashtool>
   
.. toctree::
   :maxdepth: 3
   :caption: Hilfe
   :name: sec-help   

   Fragen und Antworten <help/faq>
   Meinungen und Tipps <help/opinions>
   Bekannte Fehler <help/errors>
   Technische Unterstützung <help/support>
   Service <help/service>
   Mitarbeit <help/cooperation>
   Spenden <help/donation>
   Glossar <help/glossar>
