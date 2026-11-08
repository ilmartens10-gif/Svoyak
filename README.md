# Своя игра – Quiz mit Lobby

Browser-Quiz nach dem Vorbild der russischen TV-Show „Своя игра“ (Jeopardy). Ein Moderator erstellt eine Lobby, Freunde treten mit einem 4-stelligen Code bei und buzzern um die Fragen.

Es ist keine eigene Server-Software nötig: Die Verbindung läuft direkt zwischen den Browsern (WebRTC über [PeerJS](https://peerjs.com)).

## Auf GitHub veröffentlichen

1. Auf GitHub ein neues Repository anlegen, z. B. `svoya-igra`.
2. `index.html` und diese `README.md` hochladen (**Add file → Upload files**).
3. **Settings → Pages**: Bei *Source* „Deploy from a branch“ wählen, Branch `main` und Ordner `/ (root)`, dann speichern.
4. Nach etwa einer Minute ist die Seite unter `https://DEIN-NAME.github.io/svoya-igra/` erreichbar.

## Spielen

1. Der Moderator öffnet die Seite, gibt seinen Namen ein und klickt auf **Lobby erstellen**.
2. Die Freunde öffnen denselben Link, geben Namen und Code ein und klicken auf **Beitreten**.
3. Der Moderator startet das Spiel. Wer dran ist, wählt eine Frage, danach buzzern alle.
4. Der Schnellste antwortet mündlich. Der Moderator sieht die Antwort und klickt auf ✓ oder ✗.

## Hinweise

- Der Moderator spielt nicht mit, weil er die Antworten sieht. Er muss die Seite während des Spiels offen lassen.
- Wer die Seite neu lädt, muss erneut beitreten. Der Punktestand dieses Spielers geht dann verloren.
- In manchen Firmen- oder Schulnetzwerken wird WebRTC blockiert. Dann hilft ein anderes Netzwerk oder mobile Daten.
- Die Antworten stehen im Quelltext. Wer hineinschaut, kann schummeln.

## Fragen ändern

In `index.html` steht ganz oben im Script die Liste `Q`. Jede Kategorie hat genau vier Einträge im Format `"Frage|Antwort"` für 100, 200, 300 und 400 Punkte. Wenn du die Anzahl der Kategorien oder Fragen änderst, musst du auch `TOTAL` und die Spaltenzahl `repeat(5,1fr)` im CSS anpassen.
