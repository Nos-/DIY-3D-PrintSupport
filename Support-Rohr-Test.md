Die gleichnamige Blenderdatei dient dem Ausprobieren einer Stützstruktur für 3D-Drucke
======================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.
Hinzukommt das er stabil genug sein sollte um auch wirklich eine Stütze zu sein (Last, Vibration). Hierfür wählte ich einen Kreisring als Grundform und eine Art Voronoimuster zur Materialeinsparung.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)
* Addons: Cell-Fracture/ Cell-Fracture Tools


Vorgehen
--------

1. Einen Zylinder einfügen und ein Partikelsystem hinzufügen (alle Partikel sollen im ersten Frame emittiert werden)
2. Mittels 'Boolean-Modifier' das zu stützende Objekt vom Zylinder abziehen
3. 'Cell Fracture selected mesh objects' (zu dt.: zerbröckeln) auf den Zylinder anwenden (Das Ergebnis sollte in einem Extra-Layer erstellt werden)
4. In Layer mit dem zerbröckelten Objekt wechseln, alle Teilobjekte auswählen und mit Strg+J Joinen
5. Den 'Wireframe-Modifier' zum Objekt hinzufügen
6. Den 'Subsurface-Modifier' ebenfalls zum Objekt hinzufügen (je Nach Geschmack)
