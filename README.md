# Byg det mens du venter

Sandbox til Ferms stand. Besøgende foreslår et lille værktøj, Claude Code bygger det live, og det udgives automatisk med QR-kode.

## Opsætning (15 min)
1. Opret et **offentligt** repo på GitHub, fx `ferm-byg-det`, og push denne mappe til `main`.
2. Repo → Settings → Pages → Source: **GitHub Actions**.
3. Ret `config.js` til jeres Pages-adresse, fx `https://fermrad.github.io/ferm-byg-det/`. Commit og push.
4. Vent til workflowet er grønt (fanen Actions), og åbn adressen. Eksemplet "Hvem afkøler dårligt?" skal virke.

## Lokalt på laptoppen
- Galleri: `python3 -m http.server 8000` i mappen, åbn http://localhost:8000
- Claude Code: `claude` i mappen. Den læser CLAUDE.md og må redigere, committe og pushe uden at spørge.

## På storskærmen
Venstre halvdel: terminal med Claude Code, stor skriftstørrelse.
Højre halvdel: browser med galleriet. Det henter nye værktøjer hvert 30. sekund.

Fra push til live link går der typisk 1-2 minutter.

Alle data i `data/` er fiktive.
