# Novela stavebního zákona 2026 — sběrna zdrojů

**Web:** https://taiemnik.github.io/stavebnizakon/

Veřejná sbírka zdrojů k velké novele stavebního zákona (sněmovní tisk 67, senátní tisk 272). Úřední dokumenty – zákon, sněmovní a senátní tisky, pozměňovací návrhy, stenozáznamy rozprav, hlasování a usnesení – jsou tu zkopírované i převedené do textu. K tomu pracovní konsolidované znění zákonů po novele a rozcestník dalších zdrojů (web a podcast Ministerstva pro místní rozvoj, stanoviska institucí, články): u nich je jen krátký popis a odkaz na originál.

Cíl: aby se v novele mohl zorientovat každý – vlastník pozemku, stavebník, soused stavby, obec, úředník – a aby si celé repo mohl dát svému AI asistentovi a ptát se ho, co je nového a jak se ho změna týká. Návod: [AI-NAVOD.md](AI-NAVOD.md). Novinky: [CO-JE-NOVEHO.md](CO-JE-NOVEHO.md).

> Iniciativa tajemníka Městského úřadu Kopřivnice pro kolegy z úřadů i pro veřejnost – není to oficiální stránka státu ani metodika ministerstva. Konsolidované znění je strojově sestavená pracovní pomůcka; závazné je jen znění vyhlášené ve Sbírce zákonů. Popisy zdrojů jsou stručné a neutrální – názor si udělejte z originálu. Za odpovědi vašeho AI asistenta nikdo neručí; u konkrétní stavby se obraťte na stavební úřad.

## Kde je zákon teď

- **12. 12. 2025 – Předložení:** Skupina deseti poslanců předložila návrh Sněmovně. Přibylo 854 stran dokumentů, celkem od předložení 854 stran.
- **28. a 30. 1. 2026 – 1. čtení:** Obecná rozprava, návrh přikázán výborům. Přibylo 52 stran dokumentů, celkem od předložení 906 stran.
- **30. 4. 2026 – Komplexní pozměňovací návrh:** Výbor pro veřejnou správu a regionální rozvoj přijal komplexní pozměňovací návrh, který text z velké části přepsal (tisk 67/10 rozeslán 4. 5.). Přibylo 294 stran dokumentů, celkem od předložení 1 200 stran.
- **27. 5. – 11. 6. 2026 – 2. čtení:** Poslanci podali pozměňovací návrhy. Přibylo 2 871 stran dokumentů, celkem od předložení 4 071 stran.
- **3. – 10. 7. 2026 – 3. čtení:** Sněmovna návrh schválila: 88 pro, 79 proti. Přibylo 24 stran dokumentů, celkem od předložení 4 095 stran.
- **23. 7. 2026 – Postoupení Senátu:** Sněmovna postoupila schválený zákon Senátu jako senátní tisk 272. Přibylo 259 stran dokumentů, celkem od předložení 4 354 stran.
- **20. 8. 2026 – Senát zamítl:** 55 senátorů pro zamítnutí, 7 proti. Přibylo 11 stran dokumentů, celkem od předložení 4 365 stran.
- **9. 9. 2026 – Sněmovna setrvala:** Veto přehlasováno: 105 pro, 52 proti, potřeba 101. Přibylo 263 stran dokumentů, celkem od předložení 4 628 stran.
- **17. 9. 2026 – Podpis prezidenta:** Prezident zákon podepsal.
- **19. 10. 2026 – Odesláno do Sbírky:** Zákon odeslán k vyhlášení ve Sbírce zákonů.
- **1. den měsíce po vyhlášení – První vlna účinnosti:** Část ustanovení podle Čl. LXXXV písm. a), mimo jiné všechna přechodná ustanovení (Čl. II).
- **1. 1. 2027 – Hlavní účinnost:** Novela platí obecně; vzniká Úřad rozvoje území České republiky (Čl. II bod 1).
- **1. 1. 2028 – Přechod na stát:** Obecní a krajské stavební úřady zanikají 31. 12. 2027; jejich působnost i zaměstnanci přecházejí na úřady rozvoje území krajů (přechodná ustanovení, Čl. II body 9, 10 a 14). Ruší se zákon o JES.

## Co tu je

| Cesta | Obsah |
|---|---|
| `CO-JE-NOVEHO.md` | Stav procesu, nejbližší termín a co ve sbírce nově přibylo |
| `index.html` | Hlavní stránka: medailonky všech zdrojů s odkazy |
| `cistopis.html` | Prohlížeč konsolidovaného znění (hledání, osnova, filtr účinnosti) |
| `cistopis/` | Konsolidovaná znění – jeden soubor na zákon, `283-2021.md` = stavební zákon; `_ucinnost.md` = účinnost a přechodná ustanovení novely |
| `cistopis/info/` | Rejstřík změněných paragrafů, výtah jen změn, znění před novelou, jak znění vzniklo, validace |
| `zdroje/psp/` | Poslanecká sněmovna: tisky 67/0–67/15, pozměňovací návrhy, stenozáznamy, hlasování, usnesení |
| `zdroje/senat/` | Senát: tisky 272/0–272/4, stenozáznam, hlasování, usnesení |
| `zdroje/souvisejici/` | Související předpisy (státní zaměstnanci, vnitřní správa, sítě elektronických komunikací) |
| `KATALOG.md` | Přehled všech zdrojů v textu – úřední kopie i odkazy na neúřední zdroje |
| `katalog.json` | Totéž strojově (id, sekce, typ, vydavatel, datum, originál, soubory) |
| `llms.txt` | Rozcestník pro AI nástroje |
| `ai/` | Balík souborů pro AI asistenty a NotebookLM |

Ke každému PDF nebo DOCX je vedle soubor `.md` se stejným názvem: automatický převod do textu pro čtení a AI. Při citaci ověřte v originálu – odkaz je v hlavičce každého textu.

## Zdroje a autorská práva

- **Kopie** jsou jen úřední díla podle § 3 písm. a) autorského zákona (právní předpisy, návrhy právních předpisů, sněmovní a senátní publikace), staženo z psp.cz a senat.cz.
- **Neúřední zdroje** (weby a metodiky ministerstev, stanoviska, články, podcasty) se nekopírují. U každého je vlastní krátký popis a odkaz na originál.
- Konsolidované znění, popisy zdrojů a ostatní vlastní texty: Josef Procházka, tajemník Městského úřadu Kopřivnice, licence [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.cs) (plné znění v souboru [LICENSE](LICENSE)) – můžete je volně používat s uvedením zdroje. Úřední díla licenci nepodléhají.

## Chyby a doplnění

Našli jste chybu nebo chybí důležitý veřejný zdroj? Napište přes [Issues](https://github.com/taiemnik/stavebnizakon/issues).

*Aktualizováno: 22. 10. 2026*
