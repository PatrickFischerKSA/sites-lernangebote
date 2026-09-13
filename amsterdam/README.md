# Rafael & Sabine in Amsterdam

Ein statischer, mobiloptimierter Amsterdam-Reiseführer. Keine Datenbank, kein Build-Schritt und kein Tracking. Besuche, Favoriten, Notizen und die Merkliste werden nur im `localStorage` des Browsers gespeichert.

## Lokal starten

Wegen Service Worker und Standortfunktion sollte die Seite über einen lokalen Webserver laufen:

```bash
python3 -m http.server 8080 --directory amsterdam-guide
```

Danach `http://localhost:8080` öffnen. Geolocation funktioniert lokal sowie im veröffentlichten Betrieb über HTTPS.

## Testen

- In den Browser-Entwicklungswerkzeugen eine iPhone-Ansicht wählen.
- Karte, Filter, „Überspringen“, Favoriten, Besuchsstatus und Notizen testen.
- Standortzugriff einmal erlauben und einmal ablehnen.
- Unter „Application“ Manifest und Service Worker kontrollieren.
- Offline-Modus nach einem vollständigen ersten Laden testen. Kartenkacheln und Fotos werden beim erstmaligen Abruf gecacht, sind aber nur für bereits geladene Ausschnitte offline verfügbar.

## Auf GitHub Pages veröffentlichen

1. Den Inhalt dieses Ordners in ein GitHub-Repository committen und pushen.
2. In **Settings → Pages** als Quelle **Deploy from a branch** wählen.
3. Branch `main`, Ordner `/ (root)` wählen und speichern.
4. Die von GitHub angezeigte HTTPS-Adresse öffnen.

Alle Pfade sind relativ und funktionieren deshalb auch unter `username.github.io/repository-name/`.

## Bildnachweis und Aktualität

Die Ortsbilder werden von Unsplash geladen. Kartenmaterial: OpenStreetMap-Mitwirkende. Öffnungszeiten, Preise und City-Card-Leistungen sind bewusst nicht fest einprogrammiert; jede Attraktion verlinkt auf ihre offizielle Seite. Diese Angaben bitte vor dem Besuch prüfen.
