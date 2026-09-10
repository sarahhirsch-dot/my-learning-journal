# Tag 2

## Was habe ich gelernt?
Ich habe gelernt, wie man mit VS Code und Git über die grafische Oberfläche arbeitet, ohne dafür das Terminal zu brauchen: Dateien stagen (über das "+"-Symbol in der Source-Control-Ansicht), committen (einen Snapshot mit Nachricht speichern) und pushen (zu GitHub hochladen). Außerdem habe ich verstanden, dass es zwei Wege gibt, ein Projekt zu starten – entweder zuerst lokal anlegen und danach mit `git remote add origin` mit GitHub verbinden, oder umgekehrt zuerst auf GitHub anlegen und dann per "Clone" lokal herunterladen (dabei wird die Verbindung zu GitHub automatisch mit eingerichtet).

## Welches Problem hatte ich?
Ich habe den geklonten Ordner zuerst nicht wiedergefunden, weil ich beim Klonen nicht bewusst auf den Speicherort geachtet habe. Außerdem bin ich in einen "detached HEAD"- Zustand geraten und habe nicht verstanden, warum `git push` mit dem Branch "main" nicht
funktioniert hat.

## Wie habe ich es gelöst?
Beim erneuten Klonen habe ich bewusst den Desktop als Speicherort ausgewählt, damit ich den Ordner sicher wiederfinde. Das "detached HEAD"-Problem habe ich mit `git checkout -b main` gelöst – das erstellt einen echten Branch namens main genau an
meinem aktuellen Commit.