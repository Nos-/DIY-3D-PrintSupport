Die gleichnamige Blenderdatei dient dem Ausprobieren eines Voronoikäfigs-Effektes
=================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)
* Addons: Cell-Fracture/ Cell-Fracture Tools


Vorgehen
--------

1. Zum Würfel ein Partikelsystem hinzufügen (alle Partikel sollen im ersten Frame emittiert werden)
2. 'Cell Fracture selected mesh objects' (zu dt.: zerbröckeln) auf den Würfel anwenden (Das Ergebnis sollte in einem Extra-Layer erstellt werden)
3. In Layer mit dem zerbröckelten Objekt wechseln, alle Teilobjekte auswählen und mit Strg+J Joinen
4. Den 'Wireframe-Modifier' zum Objekt hinzufügen
5. Den 'Subsurface-Modifier' ebenfalls zum Objekt hinzufügen (je Nach Geschmack)

