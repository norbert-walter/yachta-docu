Funktionsweise
==============

Der Windsensor Yachta ist ein Anemometer mit rotierendem Schalenrad. Die Windrichtung wird über die Windfahne gemessen. Die Windfahne richtet sich entsprechend der Windrichtung aus. An der Unterseite der Achse befindet sich ein Neodym-Magnet, dessen Magnetfeld von einem Magnetfeldsensor (AS5600) berührungslos gemessen wird, der sich auf der grünen Platine in der Mitte befindet. Die Winkel werden in 4096 Teilschritte pro 360° unterteilt und über den I2C-Bus zum Mikrocontroller ESP8266 übertragen, so dass sich eine Winkelauflösung von ca. 0,1° ergibt. Die Windgeschwindigkeit wird über das Schalenrad gemessen, an dessen oberer Achse sich ein Kranz mit mehreren kleinen Magneten befindet. Die Magnete bewegen sich bei der Drehung an einen Hallsensor vorbei und lösen ein digitales Schaltsignal aus, das vom ESP8266 ausgewertet wird. Die Firmware des Windsensors enthält einen AccessPoint und einen kleinen Websever mit dem die Messdaten per WiFi übertragen werden können. Mit einem Handy kann man sich in das WiFi-Netzwerk des Windsensors einbuchen und die Messdaten mit einem Webbrowser ansehen. Es gibt auch eine Android-App mit der die Messdaten angezeigt werden können. Der Windsensor lässt sich aber auch über den TCP-Port 6666 mit anderer Auswerte- und Anzeigesoftware verbinden die in der Lage ist, NMEA0183 Daten auszuwerten.

.. image:: ../pics/NMEA_Bus.png
             :scale: 35%

.. todo::
	<model-viewer src="https://open-boat-projects.org/wp-content/uploads/2025/09/Yachta.glb" ar ar-modes="webxr scene-viewer quick-look" camera-controls tone-mapping="neutral" poster="poster.webp" shadow-intensity="1">
		<div class="progress-bar hide" slot="progress-bar">
			<div class="update-bar"></div>
		</div>
		<button slot="ar-button" id="ar-button">
			View in your space
		</button>
		<div id="ar-prompt">
			<img src="https://modelviewer.dev/shared-assets/icons/hand.png">
		</div>
	</model-viewer>