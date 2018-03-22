Die gleichnamige Blenderdatei dient dem Ausprobieren einer Stützstruktur für 3D-Drucke
======================================================================================

Fürs 3D-Drucken werden häufig Stützstrukturen (sog. Support) benötigt. Diese sollen möglichst guten Halt bei gleichzeitig minimalen Materialverbrauch bieten.
Hier ein naiver, nicht zu empfehlender, Ansatz.

Voraussetzungen
---------------

* Blender 2.79 (im Test verwendet)


Vorgehen
--------

1. Eine Kugel als zu stützendes Objekt einfügen
1. Einen Kegel als Stützkegel unter der Kugel einfügen
2. Mittels 'Boolean-Modifier' das zu stützende Objekt vom Kegel abziehen
