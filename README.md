# Nathalie.jobb
Vakter og lønnsestimering for Nathalie (hjemmesykepleien, Tønsberg kommune).

Appen er en vanlig nettside som kan legges på Hjem-skjermen. Den trenger ingen innlogging, og alt lagres på telefonen.

| Fil | Hva |
|---|---|
| `index.html` | Selve appen: oversikt, kalender, uker, lønn og oppsett |
| `plan.js` | Turnusplanen (vakter, vaktkoder, timesummer) |
| `manifest.webmanifest`, `sw.js`, `*.png` | Hjem-skjerm-app, ikon og offline-støtte |
| `Årsturnus 2026 – Sandåker, Nathalie.html` | Den gamle versjonen, beholdt for referanse |

## Ny turnusplan
Oppdater `plan.js`: legg inn vaktene, sett `range` til periodene planen dekker, og gi `version` en ny verdi.
Neste gang appen åpnes, oppdateres datoene i `range`. Vakter som er byttet på telefonen, blir stående.

## Slik regnes lønnen
- Fast månedslønn = årslønn × stillingsprosent ÷ 12, utbetalt den 20. for hele kalendermåneden.
- Tillegg for forrige måned (1. til siste dag) utbetales sammen med lønnen.
- Timelønn = årslønn ÷ 1850 (35,5 t/uke) eller 1950 (37,5 t/uke).
- Tillegg etter KS HTA kap. 1 § 5–6, regnet ut fra vaktenes klokkeslett: kveld 17–21, natt 21–06,
  lørdag/søndag og helligdag (133⅓ %, fra kl. 12 på aftener). Satsene endret seg 1.10.2026 og kan endres i appen.
- Skatt er et prosenttrekk, med halv skatt i desember.
