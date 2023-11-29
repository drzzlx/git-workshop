
# Wie Git funktioniert

## Technischer Unterschied zwischen SVN und GIT
Andere version control systeme, speichern Informationen als eine Liste von Änderungen pro File (Dazu gehört auch Subversion). Das nennt sich **_DELTA-BASED_** version control.

![img.png](images/delta-based-vcs.png)

## Git macht das anders:
Git verwaltet nur Snapshots von den einzelnen Dateien. Jedes Mal, wenn committed wird, wird der status des Projekts gespeichert. 

Dabei wird ein Snapshot von allen Files gemacht **- nur von denen, die sich geändert haben (!)-** und eine Referenz auf diesen Snapshot wird gespeichert.

==> Git ist ein **stream** aus **Snapshots**.

![img.png](images/file-snapshots.png)

Fast alle Git operationen können lokal ausgeführt werden. Das heißt: git ist durch eine Netzwerkverbindung kaum eingeschränkt.

In git gibt es für alles eine **Prüfsumme**. Daher können Inhalte in einem Git Repo nicht verändert werden, ohne, dass Git das mitbekommt. Es können **keine** informationen verlorgen gehen, ohne, dass Git bemerkt was genau fehlt.

Daten in git werden ausschließlich per Hash gespeichert, was einen Datenbankleak unbrauchbar machen würde.

Generell ist es relativ schwierig in git aktionen auszuführen, die man nicht widerrufen kann. Dazu kommt, dass eingecheckte Änerungen so gut wie nicht verloren gehen können.
