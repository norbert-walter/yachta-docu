Funktionsweise
==============

Der Windsensor Yachta ist ein Anemometer mit rotierendem Schalenrad. Die Windrichtung wird über die Windfahne gemessen. Die Windfahne richtet sich entsprechend der Windrichtung aus. An der Unterseite der Achse befindet sich ein Neodym-Magnet, dessen Magnetfeld von einem Magnetfeldsensor (AS5600) berührungslos gemessen wird, der sich auf der blaueb Platine in der Mitte befindet. Die Winkel werden in 4096 Teilschritte pro 360° unterteilt und über den I2C-Bus zum Mikrocontroller ESP8266 übertragen, so dass sich eine Winkelauflösung von ca. 0,1° ergibt. Die Windgeschwindigkeit wird über das Schalenrad gemessen, an dessen oberer Achse sich ein Kranz mit mehreren kleinen Magneten befindet. Die Magnete bewegen sich bei der Drehung an einen Hallsensor vorbei und lösen ein digitales Schaltsignal aus, das vom ESP8266 ausgewertet wird. Die Firmware des Windsensors enthält einen AccessPoint und einen kleinen Websever mit dem die Messdaten per WiFi übertragen werden können. Mit einem Handy kann man sich in das WiFi-Netzwerk des Windsensors einbuchen und die Messdaten mit einem Webbrowser ansehen. Es gibt auch eine Android-App mit der die Messdaten angezeigt werden können. Der Windsensor lässt sich aber auch über den TCP-Port 6666 mit anderer Auswerte- und Anzeigesoftware verbinden die in der Lage ist, NMEA0183 Daten auszuwerten.

.. raw:: html

	<!-- 3D Model-Viewer -->
	<!-- More infos: https://modelviewer.dev/docs -->
	<model-viewer
		src=" https://yachta-docu.readthedocs.io/de/latest/_static/files/Yachta.glb"
		poster="https://yachta-docu.readthedocs.io/de/latest/_images/Wind_Sensor_Yachta_tr.png"
		alt="Mein 3D-Modell"
		shadow-intensity="1"
		tone-mapping="cineon"
		camera-orbit="45deg 45deg 4m"
		interaction-prompt="none"
		ar
		camera-controls
		style="width: 400px; height: 400px; border: 0px solid #ccc; border-radius: 0px;">
	</model-viewer>

	<!-- Model-Viewer Skripte -->
	<script type="module"
	  src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js">
	</script>
	<script nomodule
	  src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js">
	</script>

Abb.: 3D-Modell Windsensor Yachta

.. raw:: html

	<!-- 3D Model-Viewer -->
	<!-- More infos: https://modelviewer.dev/docs -->
	<model-viewer
		src=" https://yachta-docu.readthedocs.io/de/latest/_static/files/Yachta_PCB_V2.1.glb"
		poster="https://yachta-docu.readthedocs.io/de/latest/_images/PCB_Yachta_V2.1_Top.png"
		alt="Mein 3D-Modell"
		shadow-intensity="1"
		tone-mapping="cineon"
		camera-orbit="45deg 45deg 4m"
		interaction-prompt="none"
		ar
		camera-controls
		style="width: 400px; height: 400px; border: 0px solid #ccc; border-radius: 0px;">
	</model-viewer>

	<!-- Model-Viewer Skripte -->
	<script type="module"
	  src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js">
	</script>
	<script nomodule
	  src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js">
	</script>

Abb.: 3D-Modell Yachta-Platine 
