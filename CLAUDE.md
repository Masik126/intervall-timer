# Intervall-Timer (Kampfsport/Ringen)

Mobil-first Intervall-Timer als Web-App. Eine Datei `index.html` (HTML/CSS/JS, kein Framework).

## Über den Nutzer
- Heißt Goat. Locker auf Deutsch, kurz, direkt, ehrlich.
- Keine Gedankenstriche (– oder —) in Texten.
- Variablennamen kurz halten.
- Hat einen Mac und ein iPhone.
- Vor großen Strukturänderungen fragen.

## Plattform
- Start als PWA, Kumpels nutzen sie per Link und legen sie über "Zum Home-Bildschirm" ab. Hosting kostenlos über GitHub Pages.
- Später evtl. zusätzlich native iPhone-App (SwiftUI) nur für Goat, ohne 99 € Apple Developer Program (kostenlose Apple-ID, SideStore oder wöchentlich über Xcode neu aufspielen).

## Ziel
"Der perfekte Timer": alles individuell anpassbar. Andere Timer-Apps lassen sich nicht genau einstellen.

## Features (Spezifikation)
1. Layout mobil-first. Oben Leiste mit pillenförmigen Tab-Buttons: "Klassisch" und "Wrestling Mode".
2. Klassisch: Rundendauer, Pausendauer, Anzahl Runden einstellbar.
3. Speicherslots: mind. 5, benennbar (z. B. "Boxpratzen"), ein Klick lädt alles inkl. Modus und Marker.
4. Marker: mehrere Zeitstempel pro Runde mit Extra-Sound. Jeder Marker schaltet zwischen Spurt und locker (z. B. ab 2:00 Spurt, ab 2:30 locker, oder Runde auslaufen lassen). Muster A gilt für jede / jede 2. / jede 3. Runde, Muster B für die Runden dazwischen (z. B. abwechselnd hart und locker).
5. Letzte 5 Sekunden einer Runde: jede Sekunde ein Piep, Bildschirm blinkt Rot und Standardfarbe (im kryptischen Modus Rot und Schwarz).
6. Ende der Pause: eigener "Get Ready"-Sound.
7. Wrestling Mode: gleiche Zeiteinstellungen. Zufällige Kommandos: Shoot, Sprawl, Downblock, Jump (hochspringen, Knie zur Brust). KEIN Roll. Gleiches Kommando darf mehrfach hintereinander kommen.
   - Umschalter "Normal" (Stimme sagt Kommando) und "Kryptisch" (Klatschen: 1x Shoot, 2x Sprawl, 3x Downblock, 4x Jump).
   - Kryptisch schaltet die ganze Seite auf Dark Mode, Normal auf Standardfarbe Beige.
   - Schwierigkeit: Beginner mind. 2,5 s Abstand (meist bis 4 s), Intermediate mind. 2 s (meist bis 3 s), Expert 1,2 bis 2,6 s. Nur Untergrenzen, Abstände komplett zufällig und gern auch mal länger, damit kein Rhythmus erkennbar ist.
8. Farben: Standard hell Beige (nicht Weiß), Kryptisch dunkel.
9. Sounds: später feste Sound-Bibliothek (gibt Goat vor), jedem Ereignis zuordenbar (Rundenstart, Rundenende, Marker Spurt, Marker locker, Get Ready, Countdown). Auch Meme-Sounds (z. B. Dustin Poirier "It's gonna be bad"). Aktuell synthetische Platzhalter-Töne.
10. Bewerten-Button: Bewertung und Verbesserungsvorschläge abschicken, Goat will sie lesen (z. B. Formspree oder Supabase, kostenlos).

## Stand index.html
- Fertig: Tabs, Zeiten mit Plus/Minus (gedrückt halten = schnell), Marker mit Muster A/B, Countdown-Piep und rotes Blinken, Get-Ready-Sound, Wrestling Normal/Kryptisch mit Dark Mode, drei Stufen mit zufälligen Abständen, Speicherslots in localStorage (5, erweiterbar bis 10), Wake Lock.
- Offen: echte Sounds und Sound-Zuordnung, Bewerten-Button, PWA-Manifest und Icon, Hosting auf GitHub Pages, Hintergrund-Problem (Töne laufen bei ausgeschaltetem Bildschirm auf dem iPhone nicht zuverlässig).

## Nächste Schritte
1. CLAUDE.md anlegen, git init. (erledigt)
2. index.html lokal testen (auch Handy-Größe), alle Bugs fixen, besonders: schaltet Kryptisch wirklich auf Dark Mode um?
3. PWA (manifest.json, Icon, apple-touch-icon), damit sie auf dem iPhone-Home-Bildschirm wie eine App aussieht.
4. Auf GitHub Pages veröffentlichen, Link an Goat.
