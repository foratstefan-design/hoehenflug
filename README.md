# Höhenflug auf GitHub

Ein Pixel-Flugquiz. Jeden Tag erzeugt ein automatischer Job neue Fragen aus Wikidata.

## In 5 Schritten online stellen
1. Auf github.com anmelden. Oben rechts **+** → **New repository**. Name: `hoehenflug`, **Public**, dann **Create repository**.
2. Auf der leeren Repo-Seite **uploading an existing file** wählen. Alle entpackten Dateien und Ordner hineinziehen: `index.html`, `scripts`, `data`, `.nojekyll`, `README.md`. Unten **Commit changes**.
3. Den versteckten Ordner `.github` kann man oft nicht hochziehen. Deshalb: **Add file → Create new file**, als Name `.github/workflows/daily.yml` tippen (die Schrägstriche legen die Ordner an), den Inhalt der Datei `daily.yml` einfügen, **Commit changes**.
4. **Settings → Pages**: bei Source **Deploy from a branch**, Branch **main**, Ordner **/ (root)**, **Save**. Nach 1 bis 2 Minuten steht oben der Link: `https://DEINNAME.github.io/hoehenflug/`
5. Oben auf **Actions** → **Tägliche Fragen** → **Run workflow**. Falls GitHub fragt, Workflows aktivieren. Nach 3 bis 5 Minuten liegen unter `data/days/` die Fragen für heute und morgen. Danach läuft es jeden Tag von allein.

Falls der Job rot wird mit einer Fehlermeldung zum Speichern: **Settings → Actions → General → Workflow permissions → Read and write permissions** einschalten und den Job nochmal starten.

## Hinweise
- Ohne Tagesdatei läuft die Seite trotzdem mit den eingebauten Fragen.
- Premium-Modi zum Testen freischalten: `#premium` an die Adresse hängen. Zum Bezahlen braucht es später einen Bezahldienst.
- Rekorde stehen nur im Browser des Spielers.
