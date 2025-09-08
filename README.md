# Datenverarbeitung in der Medienproduktion: Terrain Generator

Dieses Repository enthält die Endabgabe für das Modul Datenverabeitung in der Medienproduktion.

Hierbei sollten wir zu bestimmte Überkategorien mit den Geometry Nodes in Blender und dem Blender Scripting ein Projekt ausarbeiten.

Wir entscheiden uns dabei für einen Terrain Generator, der auf Basis eines farblich markierten Pixel-Rasters ein Environment in Blender generieren soll.

## Beispiel Pattern

  <img src="./Pattern\pattern_20x20.png" width="300px" />

Jeder markierte Pixel soll später für bestimmte Umgebungsobjekte in der Blender Szene geneiert werden.

## Beispielergebnis

<img src="./E:\Projekte\HFU\DVMP\Pattern\HFU_render.png" />

## Zugang zur Abschlusspräsentation

📄 [Präsentation ansehen](./Abschlusspräsentation.pdf)

## BENÖTIGTE SOFTWARE: 
    - Blender >3.0
    - Python
    - cv2 (opencv-python)
        - in der Blender Python.exe installieren (https://blender.stackexchange.com/questions/5287/using-3rd-party-python-modules)

Falls gewünscht kann ein eigenes Pattern erstellt werden. Es sind jedoch Test Pattern im Ordner zu finden: 
    - \DVMP\Pattern

## EIGENE PATTERN ERSTELLEN:
    1. Diese 4 Farben nutzen
        Gras: green = (0, 255, 0)
        Busch: darkGreen = (53, 101, 20)
        Baum: brown = (143, 86, 59)
        Stein: blue = (0, 0, 255)

    2. Ein Pixel entspricht einer Unit in Blender (20 x 20 Meter)

    3. Mit einem Tool deiner Wahl ein Pattern erstellen als PNG abspeichern und in den Pattern Ordner legen.


## PROGRAMM STARTEN:
    1. Blender starten

    2. Programmcode öffnen
        - Unter "terrainGeneratorPlugin.py" den "import_path" wie folgt anpassen.
            - C:/Users/.../DVMP/Exports/Gras
        - Sowie der Texturpfad in der plane_texture MEthode.
            - C:/Users/.../DVMP/Pattern/grass_tex_dark.jpg"
    
    3. In Blender Add-on installieren
        - Preferneces -> Add-ons -> terrainGeneratorPlugin.py installieren
        - Add-on aktivieren

    4. Import Pattern
        - Unter File -> Import -> Terrain Generator -> gewünschtes Pattern auswählen

Nun sollte eine Landschaft gemäß des Pattern in Blender angezeigt werden.
