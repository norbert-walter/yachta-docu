Funktionsweise
==============

Der Windsensor Yachta ist ein Anemometer mit rotierendem Schalenrad. Die Windrichtung wird über die Windfahne gemessen. Die Windfahne richtet sich entsprechend der Windrichtung aus. An der Unterseite der Achse befindet sich ein Neodym-Magnet, dessen Magnetfeld von einem Magnetfeldsensor (AS5600) berührungslos gemessen wird, der sich auf der grünen Platine in der Mitte befindet. Die Winkel werden in 4096 Teilschritte pro 360° unterteilt und über den I2C-Bus zum Mikrocontroller ESP8266 übertragen, so dass sich eine Winkelauflösung von ca. 0,1° ergibt. Die Windgeschwindigkeit wird über das Schalenrad gemessen, an dessen oberer Achse sich ein Kranz mit mehreren kleinen Magneten befindet. Die Magnete bewegen sich bei der Drehung an einen Hallsensor vorbei und lösen ein digitales Schaltsignal aus, das vom ESP8266 ausgewertet wird. Die Firmware des Windsensors enthält einen AccessPoint und einen kleinen Websever mit dem die Messdaten per WiFi übertragen werden können. Mit einem Handy kann man sich in das WiFi-Netzwerk des Windsensors einbuchen und die Messdaten mit einem Webbrowser ansehen. Es gibt auch eine Android-App mit der die Messdaten angezeigt werden können. Der Windsensor lässt sich aber auch über den TCP-Port 6666 mit anderer Auswerte- und Anzeigesoftware verbinden die in der Lage ist, NMEA0183 Daten auszuwerten.

.. image:: ../pics/NMEA_Bus.png
             :scale: 35%

.. raw:: html

   <div style="border:1px solid red; padding:5px;">
		<strong>Hallo Welt!</strong>
		<model-viewer width: 400pix; height: 400pix; src="https://modelviewer.dev/shared-assets/models/NeilArmstrong.glb"
			  alt="Mein 3D-Modell"
			  shadow-intensity="1"
			  ar
			  camera-controls
			  auto-rotate>
		</model-viewer>

		<!-- Model-Viewer Skripte -->
		<script type="module"
		  src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js">
		</script>
		<script nomodule
		  src="https://unpkg.com/@google/model-viewer/dist/model-viewer-legacy.js">
		</script>
   </div>