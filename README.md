# Sicherheitsaudit Tiefbau

Programm für Sicherheitskontrollen, Rundgänge und Audits auf der Tiefbaustelle.
Läuft vollständig im Browser, ohne Server und ohne Anmeldung. Alle Daten bleiben
auf dem Gerät, auf dem sie erfasst wurden (lokaler Gerätespeicher des Browsers).

## Was hier drin liegt

| Datei | Zweck |
|---|---|
| `index.html` | das ganze Programm in einer Datei |
| `manifest.json` | Name, Farben und Symbole der installierten App |
| `sw.js` | Offline-Zwischenspeicher, damit die App ohne Empfang startet |
| `icon*.png` | App-Symbol (Warnweste) in allen benötigten Grössen |
| `.nojekyll` | sagt GitHub Pages, dass nichts umgebaut werden soll |

## Veröffentlichen (einmalig, ca. 5 Minuten)

1. Auf **github.com** einloggen → oben rechts **+** → **New repository**
2. Name: `sicherheitsaudit` · Sichtbarkeit: **Public** · kein Häkchen bei
   „Add a README file" → **Create repository**
3. Auf der leeren Seite: **uploading an existing file** anklicken
4. **Den Inhalt** dieses Ordners hineinziehen — also `index.html`, `manifest.json`,
   `sw.js`, alle `icon*.png`, `.nojekyll` und diese `README.md`.
   Nicht den Ordner selbst, sondern die Dateien darin.
5. Unten **Commit changes**
6. Oben **Settings** → links **Pages** → unter „Build and deployment" bei
   *Source* **Deploy from a branch** wählen, Branch **main** und Ordner **/ (root)**
   → **Save**
7. Eine Minute warten, Seite neu laden. Oben steht dann die Adresse:
   `https://<dein-benutzername>.github.io/sicherheitsaudit/`

## Auf dem iPad installieren

1. Die Adresse in **Safari** öffnen (nicht Chrome — nur Safari darf auf dem
   iPhone/iPad zum Home-Bildschirm hinzufügen)
2. **Teilen**-Symbol unten → **Zum Home-Bildschirm**
3. Es erscheint die orange Warnweste mit dem Namen **Sicherheitsaudit**
4. Die App startet im Vollbild, ohne Browserleiste, und funktioniert ohne Empfang

Auf Android: Chrome öffnen → Menü → **App installieren**.

## Neue Version veröffentlichen

1. In `sw.js` die Zeile `const VERSION = 'sa-v1';` auf `'sa-v2'` erhöhen
   (sonst zeigen bereits installierte Geräte weiter die alte Fassung)
2. Beide Dateien (`index.html`, `sw.js`) im Repository ersetzen:
   Datei anklicken → Stift → Inhalt ersetzen → Commit.
   Oder einfacher: **Add file → Upload files** und beide überschreiben.
3. Nach ein bis zwei Minuten holen sich die installierten Geräte die neue Fassung
   beim nächsten Start selbst.

## Wichtig zum Datenschutz

* Das Repository ist **öffentlich** — der Programmcode und der Fragenkatalog sind
  für alle sichtbar. Das ist unbedenklich, solange hier **keine echten Baustellen-,
  Personen- oder Mängeldaten** abgelegt werden.
* Erfasste Kontrollen werden **nie** zu GitHub übertragen. Sie bleiben im Browser
  des jeweiligen Geräts.
* GitHub Pages ist nur die Auslieferung des Programms, keine Datenablage.
