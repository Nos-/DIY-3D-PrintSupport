Die gleichnamige Blenderdatei dient dem Ausprobieren einer Stützstruktur für 3D-Drucke
======================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.
Hinzukommt das er stabil genug sein sollte um auch wirklich eine Stütze zu sein (Last, Vibration). Hierfür wählte ich einen Kegel mit einer Art Voronoimuster (naja eigentlich Wireframe) zur Materialeinsparung.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)


Vorgehen
--------

1. Einen Kegel einfügen
2. Mittels 'Boolean-Modifier' das zu stützende Objekt vom Kegel abziehen
3. Den Kegel modifizieren damit er eine bessere Auflagefläche bietet
5. Den 'Wireframe-Modifier' zum Objekt hinzufügen
6. Den 'Subsurface-Modifier' ebenfalls zum Objekt hinzufügen (je Nach Geschmack)
