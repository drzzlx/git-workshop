# Wie Git funktioniert

Git speichert nicht die Veränderungen einer Datei! Sondern erstellt Snapshots der Datei und Verlinkungen zu älteren ungeänderten Dateien.

Jeder commit erhält einen einzigartigen commit-hash.

Git unterscheidet zwischen 3 Dateizuständen:
  - Modified (geändert aber noch nicht in lokaler Datenbank)
  - Staged (bedeutet, dass eine geänderte Datei in ihrem gegenwärtigen Zustand für den nächsten
Commit vorgemerkt ist)
  - Committed (bedeutet, dass die Daten sicher in der lokalen Datenbank gespeichert sind)

## Kernkonzepte von Git
- git speichert nicht die Veränderungen einer Datei, sondern erstellt Snapshots der Datei und Verlinkungen zu älteren ungeänderten Dateien
- git funktioniert im Prinzip voll und ganz lokal!
  - das heißt auch: es ist schwer, etwas kaputt zu machen!
- Git tracked nicht alle modifizierten Files 
- nur files in der Staging-Area ("index") werden für commit berücksichtigt
- jeder commit erhält einen einzigartigen commit-hash
- Git unterscheidet zwischen 3 Dateizuständen:
  - Modified (geändert aber noch nicht in lokaler Datenbank)
  - Staged (bedeutet, dass eine geänderte Datei in ihrem gegenwärtigen Zustand für den nächsten
Commit vorgemerkt ist)
  - Committed (bedeutet, dass die Daten sicher in der lokalen Datenbank gespeichert sind)
- Git ist ein simpler Key-Value-Data-Store