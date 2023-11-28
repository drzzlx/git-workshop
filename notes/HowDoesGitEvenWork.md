# Wie Git funktioniert

Git speichert nicht die Veränderungen einer Datei! Sondern erstellt Snapshots der Datei und Verlinkungen zu älteren, unveränderten Dateien.

Jeder commit erhält einen einzigartigen commit-hash. Jeder Commit kennt den (und nur den) vorherigen Commit.

Git unterscheidet zwischen 3 Dateizuständen:
  - Modified (geändert aber noch nicht in lokaler Datenbank)
  - Staged (bedeutet, dass eine geänderte Datei in ihrem gegenwärtigen Zustand für den nächsten
Commit vorgemerkt ist)
  - Committed (bedeutet, dass die Daten sicher in der lokalen Datenbank gespeichert sind)

Git funktioniert im Prinzip voll und ganz lokal

Wichtig für Kommandozeile: Nur Dateien in der Staging-Area ("index") werden für commit berücksichtigt

Git ist ein simpler Key-Value-Data-Store