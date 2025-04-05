🖼️ BMP-zu-JPEG-Konvertierungsskript für Windows
📋 Beschreibung
Dieses PowerShell-Skript überwacht einen angegebenen Ordner (inkl. Unterordner) und konvertiert automatisch alle gefundenen .bmp-Dateien in das .jpg-Format. Nach erfolgreicher Konvertierung wird die ursprüngliche .bmp-Datei gelöscht. Das Skript läuft in einer Endlosschleife und überprüft regelmäßig auf neue Dateien.

⚙️ Voraussetzungen
Windows 7 SP1 oder höher

PowerShell 2.0 oder höher (empfohlen: 5.1)

.NET Framework 4.5 oder höher (z. B. 4.8)

Lesende und schreibende Zugriffsrechte auf den Zielordner

🧾 Verwendung
Pfad anpassen
Öffne das Skript und ersetze:
$folderPath = "C:\\Pfad\\Zu\\Deinem\\Ordner"
durch den tatsächlichen Pfad, den du überwachen möchtest.

Skript starten
Führe das Skript in einer PowerShell-Konsole aus:

powershell -ExecutionPolicy Bypass -File ConvertBmpToJpeg.ps1
Was passiert dann?

Das Skript prüft alle 10 Sekunden auf neue .bmp-Dateien.

Jede gefundene Datei wird konvertiert und erhält einen Zeitstempel im Dateinamen, z. B.:
bildname_20250405_153045_123.jpg

Nach erfolgreicher Konvertierung wird die .bmp-Datei gelöscht.

Zwischen jeder Datei wird 1 Sekunde pausiert, um Namensüberschneidungen zu vermeiden.

🔄 Beispiel-Ausgabe
---------------------------------------------------------------------------------
Prüfe Ordner: C:\Temp\Test
Gefundene BMP-Dateien: 2
Konvertiere: C:\Temp\Test\bild1.bmp -> C:\Temp\Test\bild1_20250405_154025_221.jpg
Erfolgreich konvertiert: C:\Temp\Test\bild1_20250405_154025_221.jpg
Gelöscht: C:\Temp\Test\bild1.bmp
...
-----------------------------------------------------------------------------------
Warte auf neue Dateien...
🛡️ Sicherheitshinweise
Das Skript löscht die Originaldateien nach erfolgreicher Konvertierung.

Teste das Skript zuerst in einem separaten Verzeichnis, um ungewollten Datenverlust zu vermeiden.

