Die gleichnamige Blenderdatei dient dem Ausprobieren einer Stützstruktur für turmartige 3D-Drucke
=================================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.
Hinzukommt das er stabil genug sein sollte um auch wirklich eine Stütze zu sein (Last, Vibration). Hierfür wählte ich einen Kegel mit einer Art Voronoimuster (naja eigentlich Wireframe) zur Materialeinsparung.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)
* optional: 3D Print Toolbox-Addon


Vorgehen
--------

1. Das gewünschte Objekt - hier ein einfacher hoher schmaler Zylinder - einfügen
2. Kegel an gewünschter Stelle einfügen (5 Segmente sollten genügen, er sollte möglichst höher als breit sein)
3. Kegel im Editmode skalieren, sodas er den zu stützenden Bereich umschließt
4. 'Wireframe-Modifier' auf Kegel anwenden
5. mit dem 'Subdivision-Surface-Modifier' (Einstellung: 'simple') für zusätzliche Verstrebungen sorgen (Einstellung: Sudivisions etwas erhöhen)
6. Alles speichern und den 'Subdivision-Surface-Modifier' aus dem vorigen Schritt anwenden ('Apply')
7. im Editmode des Kegels per 'Extrudieren' zusätzliche Verstrebungen vom Kegel zum zu stützenden Objekt erstellen (idealerweise sollten diese zum Objekt hin ansteigend verlaufen)
8. mittels 'Subdivision-Surface-Modifier' (Einstellung: 'Catmull-Clark') allzu horizontale Verstrebungen nach dem Vorbild einer Brücke verrunden
9. etwaige Überschneidungen können per 'Boolean-Modifier' entfernt werden
10. Export (z.B.: als STL-Datei) über die blendereigene Exportfunktion oder die '3D-Print Toolbox' des gleichnamigen Addons - am besten für Objekt und Support getrennt
