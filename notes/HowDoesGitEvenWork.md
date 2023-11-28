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


------------------------------

Vergesst alles was ihr wisst über Subversion und performance!

Es werden keine Unterschiede zwischen den Dateien gespeichert, sondern nur einzelne Snapshots

Andere VCS: Speichern Informationen als eine Liste von Änderungen pro File (Dazu gehört auch Subversion). Das nennt sich **_DELTA-BASED_** version control.

### Git macht das anders:
Git verwaltet nur Snapshots von den einzelnen Dateien. Jedes mal, wenn committed wird, wird der status des Projekts gespeichert. 

Dabei wird ein Snapshot von allen Files gemacht und eine Referenz auf diesen Snapshot wird gespeichert. Bleibt eine Datei gleich, wird diese nicht dupliziert, sondern nur eine Referenz auf die Datei aus dem vorherigen Snapshot erstellt. 

Git ist ein **stream** aus **Snapshots**.

Fast alle Git operationen können lokal ausgeführt werden. Das heißt: git ist kaum durch eine Netzwerkverbindung eingeschränkt.

In git gibt es für alles eine Prüfsumme. Daher können Inhalte in einem Git Repo nicht verändert werden, ohne, dass Git das mitbekommt. Es können auch keine informationen verlorgen gehen, ohne, dass Git bemerkt was fehlt.

Daten in git werden ausschließlich per Hash gespeichert, was einen Datenbankleak unbrauchbar machen würde.

Generell ist es relativ schwierig in git aktionen auszuführen, die man nicht widerrufen kann. Dazu kommt, dass eingecheckte Änerungen so gut wie nicht verloren gehen können.