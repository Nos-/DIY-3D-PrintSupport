Die gleichnamige Blenderdatei dient dem Ausprobieren einer Stützstruktur für 3D-Drucke
======================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.
Hinzukommt das er stabil genug sein sollte um auch wirklich eine Stütze zu sein (Last, Vibration). Hierfür wählte ich einen Kegel mit einer Art Voronoimuster (naja eigentlich Wireframe) zur Materialeinsparung.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)
* Addon: 3D Print Toolbox


Vorgehen
--------

1. in der '3D Print Toolbox' die 'überhängende Flächen selektieren' lassen
2. diese mit Shift+d 'duplizieren' und mit p 'seperate selected' in ein extra Objekt packen
3. zum neu erstellten Objekt mit den Gegenstücken der überhängenden Flächen wechseln und mittels 'Subdivide' unterteilen. (Vor dem Unterteilen kann ggf. auch noch eine Unterteilung in Dreiecke ('Split Non-planar Faces') erfolgen)
4. diese mittels 'Extrude individual Faces' (gefolgt von g) ein Stück Richtung Bodenplatte extudieren (und anschließend ggf. mit Skalierung entlang der z-Achse auf etwa eine Höhe bringen: s z 0.5). Achtung: tiefer liegende Teile werden ignoriert.
(5. die noch markierte Bodenflächen für mehr Stabilität mit s etwas skalieren (größer=stabiles Gerüst, kleiner=baumstammartig))
6. Entweder mittels 'Un-Subdivide' die einzelnen Faces zu Punkten zusammenführen oder per 'Remove Doubles' (Merge Distance z.B. 0.1 zunehmend) benachbarte Punkte zusammenführen
(7. Nach 'Un-Subdivide': Mittels 'fill' (Taste f) die nun alleinstehenden Punkte wieder mit ihren jeweiligen Nachbarpunkten zu einer Fläche verbinden)
8. Die Schritte 4 bis 7 nach Bedarf wiederholen (zum Schluss sollte der Support auf der Bodenplatte aufsetzen)
(9. mithilfe des 'Subdiv-Surface-Modifiers' (Einstellung: simple) für etwas mehr Verstrebungen im Mesh sorgen)
10. die Einzelteile der bis hierhin erstellten Stützstruktur verschmelzen/ bereinigen (z.B. per 'seperate loose parts' und dann mittels Boolean 'Union')
11. mittels des 'Wireframe-Modifiers' nur noch die Kanten des Mesh (also das Gerüst) verwenden
12. zum Schluss nochmal mit dem 'Subdiv-Surface-Modifier' (Einstellung: Catmull-Clark) verrunden, damit es sich besser 3D-Drucken lässt
13. Export (z.B.: als STL-Datei) über die '3D-Print Toolbox' oder die Blendereigene Exportfunktion - am besten für Objekt und Support getrennt
