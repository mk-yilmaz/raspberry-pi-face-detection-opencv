# v1_basic_detection.py (Version 1)

Dies ist die Basis-Version meines Kamera-Projekts für den Raspberry Pi 5. Der Fokus liegt hier auf der stabilen Erkennung von Gesichtern in Echtzeit unter Verwendung klassischer Computer-Vision-Algorithmen.

# Projektbeschreibung
In diesem ersten Schritt habe ich ein System entwickelt, das mithilfe der **Haar Cascade Klassifizierung** Gesichter im Videostream identifiziert. Das Programm prüft kontinuierlich das Sichtfeld der Kamera, optimiert das Bild für die Analyse und speichert bei einer erfolgreichen Erkennung ein Foto mit Zeitstempel ab.

# Verwendete Technologien
- **Python**: Hauptprogrammiersprache.
- **OpenCV (Open Source Computer Vision Library)**: Zur Bildverarbeitung und Anwendung der Haarcascade-Algorithmen.
- **Picamzero**: Eine effiziente Bibliothek zur Ansteuerung der Raspberry Pi Hardware-Kamera.
- **Haar Cascade**: Ein maschinelles Lernmodell zur Objekterkennung (frontalface_default).

# Technische Highlights
- **Graustufen-Konvertierung**: Reduzierung der Datenkomplexität von 3 Kanälen (RGB) auf einen Kanal zur schnelleren Verarbeitung.
- **Histogramm-Egalisierung**: Automatische Kontrastverbesserung (`equalizeHist`), um die Erkennungsrate bei schwierigen Lichtverhältnissen zu erhöhen.
- **Parametrisierung**: Feinabstimmung von `scaleFactor` und `minNeighbors`, um Fehlalarme zu minimieren und die Präzision zu steigern.
- **Fehlerbehandlung**: Validierung der Hardware-Verfügbarkeit und der XML-Modelldateien vor Programmstart.

# Installation & Nutzung
1. Sicherstellen, dass die Kamera am Raspberry Pi aktiviert ist.
2. Die benötigten Bibliotheken installieren:
   ```bash
   pip install opencv-python picamzero
   ```
3. Das Skript ausführen:
   ```bash
   python picam.py
   ```


