Fragen und Antworten
====================

**Welche Bedeutung hat der Blink-Code der blauen LED?**

	Die blaue LED zeigt den Status der WiFi-Verbindung an.
	
	+--------------------------------------+-----------------------------------------------------+
	|LED Status                            | Bedeutung                                           |
	+======================================+=====================================================+
	|dauerhaft aus                         | Zu externen WiFi verbunden                          |
	+--------------------------------------+-----------------------------------------------------+
	|dauerhaft an                          | Kein externes WiFi verbunden                        |
	+--------------------------------------+-----------------------------------------------------+
	|blinkt kurzzeitig                     | Daten werden über externes WiFi übertragen          |
	+--------------------------------------+-----------------------------------------------------+
	|dauerhaft an, kurzzeitig unterbrochen | Daten werden über internes WiFi übertragen (Yachta) |
	+--------------------------------------+-----------------------------------------------------+

	Grundsätzlich wird unterschieden, ob über ein externes WiFi oder über das interne WiFi (NoWa) Daten übertragen werden. Internes WiFi bedeutet, dass man sich mit dem WiFi, das der Windsensor selber zur Verfügung stellt, verbunden hat. Beim einem externen WiFi verbindet sich der Windsensor als Client an ein anderes WiFi-Netzwerk.

	Sofern sich das Schalenrad dreht, werden Winddaten ein mal pro Sekunde übertragen. Dreht sich das Schahlenrad nicht, so wird die Datenrate reduziert. Dann wird nur alle 3 Sekunden ein Telegramm ausgesendet.

**Die Windrichtungsanzeige ist nicht korrekt**

	Je nachdem wie der 5x5x5 mm Magnet zur Windrichtungsanzeige eingeklebt ist, kann eine Abweichung im Anzeigeinstrument auftreten. Das ist nicht weiter schlimm, denn über einen **Offset** unter **Device Settings** kann der Fehler korrigiert werden.

**Die Messwerte für den wahren Wind stimmen nicht**

	Der Windsensor Yachta kann nur den relativen Wind anzeigen, da Referenzwerte der Ausrichtung des Bootes im Windsensor nicht vorliegen. Der wahre Wind kann nur korrekt angezeigt werden, wenn der Windsensor als Wetterstation stationär an Land mit korrekter Nord-Ausrichtung installiert ist. Auf einem beweglichen Boot kann nur der relative Wind bzw. scheinbare Wind angezeigt werden.

**Die Windrichtungsanzeige reagiert nicht**

    * Ist der Magnet richtig herum eingebaut?  (korrekte Nord-Süd-Ausrichtung)
    * Ist die Feldstärke des Magneten ausreichend stark? (Magn. Flux Density muss größer 1000 mT sein)
    * Ist der Abstand des Magneten zum Chip hinreichend klein? (ca. 1 mm Abstand)
    * Ist der richtige Wind Sensor Type unter Device Settings ausgewählt? (Yachta)

**Die Windspeedanzeige funktioniert nicht richtig**

    * Ist der Hallsensor nah genug am Magnetkranz? (ca. 1 mm Abstand bei Hallsensor mit langen Drähten)
    * Sind die Magnete richtig herum eingebaut? (korrekte Nord-Süd-Ausrichtung)
    * Hat die Achse zu großes Spiel? (Der Magnetkranz darf nicht hin und her pendeln und den Abstand zum Hallsensor verändern)

**Die Windspeedanzeige zeigt den doppelten Speed an**

	Das Problem wird häufig durch falsche Ausrichtung der Magnete im Magnetkranz verursacht. Die Magnete müssen eine abwechselnde Polarität haben. Sind alle Magnete gleich ausgerichtet, so werden 4 Impulse anstatt 2 Impulse erkannt. Die Geschwindigkeit ist damit um den Faktor 2 zu hoch. Am einfachsten ist es, wenn man die Magnete vor dem Einbau alle zusammen aneinander haftet und einzeln abnimmt und eine der anhaftenden Seiten markiert, z.B. immer die linke Seite. So kann man beim Einbau die Ausrichtung des Magnetfeldes sehr einfach kontrollieren. Mit einem Handkompass wäre das durchaus auch möglich, wenn auch etwas schwieriger.
	
	.. image:: ../pics/Magnets.png
             :scale: 20%

**Die Android App lässt sich nicht unter Android 11 installieren**

	Ab Android 11 wurden die Sicherheitseinstellungen verschäft und es lassen sich keine Apps (apk-Dateien) mehr von externen Quellen installieren. Das soll verhindern, dass ungewollt Programme über Internetseiten installiert werden. Jedes Mal wenn eine apk-Datei herunter geladen wird, wird deren Dateiendung automatisch umbenannt und die Datei kann nicht mehr zur Installation gestartet werden. Ein nachträgliches umbenenen der Datei in apk unter Android ist nicht möglich. Um die App trotzdem unter Android 11 installieren zu können, muss ein kleiner Umweg über die Dateitransfer-Funktion vorgenommen werden. Dazu wird die apk-Datei auf einem PC herunter geladen und über ein USB-Kabel in den Download-Ordner des Handys übertragen. Mit dem internen Datai-Manager von Android 11 kann dann die apk-Datei installiert werden.
	

**Es ist keine Verbindung mit dem Windsensor über WiFi möglich**

	Nachdem der Windsensor mit 12V versorgt wird, öffnet sich nach 30s das WiFi-Netzwerk des Windsnesors mit dem Namen Yachta. Das Passwort lautet 12345678. Einige Handy und Tabletts können nicht korekt damit umgehen, dass der AsseccPoint des Windsensors keine Internetverbindung hat. Immer wenn man die Webseite http://192.168.5.1 aufrufen möchte wird die Anfrage in das Internet geleitet anstatt zum Windsensor. Das Routing im Handy bzw. Tablett ist nicht korrekt. Das selbe Problem tritt auch bei der Android-App auf. Um den Fehler zu beheben kann man die Mobilfunk-Verbindung des Handys zum Internet trennen. Danach wird der Windsensor Yachta wieder gefunden.
	
**Wenn ich die Spannung zuschalte, dann wird in AVnav oder OpenPlotter der Windsensor nicht automatisch angebunden**

	Wird AVnav oder OpenPlotter auf einem Raspi verwendet und stellt der Raspi gleichzeitig den AccessPoint bereit mit dem sich der Windsensor verbinden soll, so dauert es eine gewisse Zeit nach dem Zusschalten der Versorgungsspannung bis das Linux-Betriebssystem hochgefahren ist und der Access Point bereit ist. Die Boot-Phase kann 2…3 min dauern. Wenn zeitgleich die Versorgungsspannung des Windsensors zugeschaltet wird, so versucht der Windsensor 30s lang sich in das externes WiFi-Netzwerk des Raspi einzubuchen. Da der Raspi aber wesentlich mehr Zeit zum Booten benötigt als der Windsensor, scheitert die Herstellung der WiFi-Verbiundung. Unter Device Settings kann das Connection Timeout von 30s auf 2 min oder mehr eingestellt werden. Dann wartet der Windsensor entsprechend länger bis das Connection-Timeout kommt. Mit der blauen LED auf der Platine kann die WiFi-Verbindung überprüft werden. Ist die LED aus, so hat sich der Windsensor in ein externes WiFi-Netzwerk als Client eingebucht. Wenn Daten übertragen werden, bitzt die blaue LED kurz auf.
	
**Die Anzeige der Daten vom Windsensor ist sehr träge**

	Wenn sich das Schalenrad nicht deht, wird das Sende-Intervall der Datentelegramme von 1s auf 3s erhöht, um  nicht unnötig viele Daten zu senden, denn bei Windstille macht es nicht viel Sinn dauerhaft die selben Daten zu senden. Wenn der Windsensor zu Hause ohne Wind getestet wird, dann kann es bis zu 3s dauern, bis Windspeed-Daten kommen, wenn man das Schalenrad dreht. Für Tests zu Hause eignet sich der Demo Mode ganz gut, bei dem permanent simulierte Daten für Windrichtung und Windspeed erzeugt werden. Die Einstellungen könne unter **Device Settings** über den **Server Mode** vorgenommen werden.
	
**Ich sehe keine Temperaturwerte**

	Wenn unter **Wind Values** kein Temperaturwert angezeigt wird, dann ist vermutlich der **Temp Sensor Type** unter **Device Settings** nicht richtig ausgewählt. Der Wert muss auf **DS18B20** stehen. Andere Temperatursensoren als der DS18B20 werden beim Windsensor Yachta nicht unterstützt.
	
**Ich sehe keine Messwerte für Luftfeuchtigkeit und Luftdruck**

	Der Temp Sensor Type BME280 kann beim Windsensor Yachta nicht verwendet werden, da er nicht auf der Platine verbaut ist. Eine Anzeige der Luftfeuchtigkeit und des Luftdrucks sind nicht möglich.
	
**Ich habe noch einen Fehler entdeckt, was kann ich tun?**

	Falls Sie noch einen Fehler entdeckt haben, so können Sie uns gerne über das Kontaktformular der Webseite informieren. Beschreiben Sie den Fehler möglichst so, dass er nachvollzogen werden kann. Wir leiten den Fehlerbericht an den jeweiligen Projekteigentümer weiter und bitten ihn um Korrektur. Sie können aber auch selber einen Fehlerbericht als `Issue`_ bei GitLab auf der Projektseite einreichen. GitLab informiert dann den Projekteigentümer automatisch.

.. _Issue: https://github.com/norbert-walter/Windsensor_Yachta/issues
	
**Ich habe hier keine Lösung für mein Problem gefunden**

	Falls Sie hier keine Lösung für Ihr Problem gefunden haben, können Sie bei GitLab unter Issues nach bekannten nicht gelösten Problemen nachsehen. Schauen Sie auch unter Closed Issues nach. Dort sind auch einige Lösungen zu aufgetretenen Fehlern beschrieben. Wenn Sie möchten, können Sie sich auch Hilfe bei anderen Seglern im Deutschen `Segeln-Forum`_ holen. Dort gibt es viele Interessierte, die bereits erfolgreich einen Windsensor Yachta zusammen gebaut haben und Ihnen helfen können. Sie können dort in Deutsch oder Englisch kommunizieren.

.. _Segeln-Forum: https://www.segeln-forum.de/board/195-open-boat-projects-org/