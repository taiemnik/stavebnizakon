# Stenozáznamy PSP/Senát — datová vrstva argumentů

Tahle složka je určená pro sběr argumentace ze stenozáznamů:

- kdo mluvil,
- jaké teze zazněly,
- jak se liší argumentace PSP vs. Senát.

## Struktura

- `_catalog.csv` — seznam zdrojových URL stenozáznamů
- `raw/` — stažené originály (HTML/TXT)
- `analyza/arguments.csv` — segmenty textu po řečnících
- `analyza/speakers.csv` — souhrn řečníků (počet vstupů, rozsah)
- `analyza/summary.md` — rychlý briefing

## Jak spustit

```powershell
python "02_Work/Projects/Stavební zákon/scripts/steno_pipeline.py"
```

## Katalog (`_catalog.csv`)

Povinné sloupce:

`source,chamber,date,title,url,note`

Příklad řádku:

```csv
psp,PSP,2026-07-10,3. čtení tisku 67 — stenozáznam,https://www.psp.cz/....,hlasování 117
```

## Důležité omezení

- Segmentace řečníků je heuristická (není to úředně ověřený přepis).
- Výstupy používej jako **analytický index**, ne jako finální citaci bez ruční kontroly.
