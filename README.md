# Arkiv – DMI WAM, södra Östersjön

Löpande arkiv av DMI:s vågmodell WAM (område *North Sea and Baltic*), utsnitt
10–21,5° Ö, 53,8–58° N. Fylls på automatiskt efter varje modellkörning av
`.github/workflows/arkivera.yml` med koden i [dyning](https://github.com/ZephXiro/dyning) (`archive.py`).

| Sökväg | Innehåll |
|---|---|
| `falt/ÅÅÅÅ/MM/DD/HHz.bin.gz` | timme 0–5 av körningen, alla fält, uint8 `[fält][timme][rad][kolumn]`, 255 = land |
| `punkter/ÅÅÅÅ-MM.json` | utfall per plats och timme |
| `prognoser/ÅÅÅÅ/MM/DD/HHz.json` | hela prognosen (0–132 h) för platserna |
| `statistik.json` | prognosfel per plats och dygn framåt, senaste 30 dygnen |
| `index.json`, `meta.json` | körningar, rutnät, fält och skalor |

Värde = heltal × `scale` i `meta.json`. Riktningar anger varifrån vågorna/vinden kommer.

Data: DMI (Danmarks Meteorologiske Institut), DMI Open Data.
