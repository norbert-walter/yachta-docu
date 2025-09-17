###############################
Windsensor Yachta Dokumentation
###############################
Letzte Aktualisierung |today|

.. image:: https://readthedocs.org/projects/yachta-docu/badge/?version=latest
    :target: https://yachta-docu.readthedocs.io/de/latest/?badge=latest
    :alt: Documentation Status

.. note::
   Diese Seiten sind noch in Bearbeitung.

.. image:: /pics/Wind_Sensor_Yachta_tr.png
             :scale: 100%

Der Windsensor Yachta dient zur Messung der Windgeschwindigkeit und der Windrichtung auf Booten. Er wird am Mast installiert und mit 12V versorgt. Die Datenübertragung der NMEA0183 Telegramme erfolgt drahtlos per WiFi. Im Windsensor befindet sich ein Access Point und ein kleiner Webserver. Als Messwertanzeige dient ein Handy mit einen Webbrowser. Es gibt ebenfalls eine Android-App mit der die Daten angezeigt werden können. Die Messdaten lassen sich auch in anderen Programmen wie `SignalK`_, `AvNav`_, `OpenCPN`_, `Navionics`_ oder auf Geräte wie das `OBP60`_ oder den `OBP-Plotter`_ übertragen und angezeigen.

.. _SignalK: https://signalk.org/
.. _AvNav: https://www.wellenvogel.net/software/avnav/docs/beschreibung.html
.. _OpenCPN: https://opencpn.org/
.. _Navionics: https://play.google.com/store/apps/details?id=it.navionics.singleAppMarineLakesHD&hl=de
.. _OBP60: https://obp60-v2-docu.readthedocs.io/de/latest/
.. _OBP-Plotter: https://obp-plotter-v4-info.readthedocs.io/de/latest/


Der Windsensopr Yachta ist so konzipiert, dass er als DIY-Projekt nachgebaut werden kann. Alle technischen Unterlagen stehen als Open Hardware, Open Source und Open Data zur Verfügung und sind bei `GitHub`_ veröffentlicht. Für den einfachen Nachbau kann über Open Boat Projects eine bestückte, programmierte und getestete Platine erworben werden. Der Nachbau beschränkt sich dann größtenteils auf die Beschaffung von mechanischen Komponenten, die Erstellung von 3D-Teilen und den machanischen Zusammenbau. Der Windsensor Yachta wurde schon über 200 Mal erfolgreich nachgebaut und hat eine große weltweite Fangemeinde. Der Service und Support erfolgt über das `Segeln-Forum`_ in deutscher oder englischer Sprache. Dort helfen kompetente Forenmitglieder, die selber einen Windsensor Yachta zusammengebaut haben. Das Core-Entwicklerteam ist dort auch anzutreffen.

.. _GitHub: https://github.com/norbert-walter/Windsensor_Yachta
.. _Segeln-Forum: https://segeln-forum.de

.. toctree::
   :maxdepth: 3
   :caption: Einführung
   :name: sec-intro

   Historie <intro/historie>
   Technische Daten <intro/specification>
  
.. toctree::
   :maxdepth: 3
   :caption: Zusammenbau
   :name: sec-assembling
   
   Funktionsweise <assembling/functionality>
   Geräteaufbau <assembling/device>
   Vorbereitung <assembling/preparation>
   Bauteilliste <assembling/partlist>
   Durchführung <assembling/actionsteps>
   Funktionstest <assembling/tests>
  
.. toctree::
   :maxdepth: 3
   :caption: Bedienung
   :name: sec-usermanual

   Inbetriebnahme <usermanual/start>
   Konfiguration <usermanual/configuration>
   Bussysteme <usermanual/bussystems>
   Datenaustausch <usermanual/dataexchange>
   Erweiterungen <usermanual/extensionss>
   Beispielkonfiguration <usermanual/samples>
   Sicherheitshinweise <usermanual/safety>
   
.. toctree::
   :maxdepth: 3
   :caption: Programmierung
   :name: sec-programming   

   Programmierumgebung <programming/environment>
   Kompilieren und Download <programming/activating>
   Web-Flashtool <programming/webflashtool>
   
.. toctree::
   :maxdepth: 3
   :caption: Infos
   :name: sec-help   

   Fragen und Antworten <help/faq>
   Meinungen und Tipps <help/opinions>
   Bekannte Fehler <help/errors>
   Technische Unterstützung <help/support>
   Service <help/service>
   Mitarbeit <help/cooperation>
   Spenden <help/donation>
   Copyright <help/copyright>
   Glossar <help/glossar>
