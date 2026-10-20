# Byg det mens du venter — instruks til Claude Code

Vi står på en IT-talentmesse. En besøgende foreslår et lille værktøj, og du bygger det live på storskærmen på 5-10 minutter. Hastighed og et synligt resultat er vigtigere end perfektion.

## Regler
- Hver idé bliver én ny mappe: `features/<kort-slug>/index.html`. Én fil, HTML + CSS + JS inline. Ingen build-trin, ingen npm.
- Brug fælles stil: `<link rel="stylesheet" href="../../assets/ferm.css">` og klasserne beskrevet i toppen af den fil.
- Data: brug filerne i `data/` (fiktive, semikolon-separeret CSV) via `fetch('../../data/<fil>.csv')`. Opfind ikke nye data, hvis de eksisterende passer.
- Biblioteker kun fra cdnjs.cloudflare.com, fx Chart.js. Pin versionen.
- Al tekst på dansk. Kort og konkret.
- Tilføj featuren øverst i `features.json`: `{ "slug", "titel", "beskrivelse", "foreslaaet_af", "tid" }` (tid = HH:MM).
- Når du er færdig: `git add -A && git commit -m "Ny feature: <titel>" && git push`. Spørg ikke om lov til commit/push i dette repo.
- Hold svarene korte i terminalen. Publikum kigger med.

## Hvis idéen er for stor
Byg den mindste version, der viser kernen, på under 10 minutter. Sig det i én sætning.

## Data
- `data/fjernvarme-maalere.csv`: 12 målere, timeværdier en uge. Kolonner: maaler_id; bygningstype; tidspunkt; forbrug_kwh; fremloeb_c; retur_c. To målere har dårlig afkøling (lav forskel mellem frem- og returløb).
- `data/vand-natforbrug.csv`: 5 forsyningszoner, 30 døgn. Kolonner: zone; dato; natforbrug_m3_t; tryk_bar; antal_maalere. Én zone får en lækage undervejs.
