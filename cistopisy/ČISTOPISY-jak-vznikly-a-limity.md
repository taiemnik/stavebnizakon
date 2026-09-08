---
created: 2026-06-18
type: project-note
topics: [Legislativa, Stavební zákon, Čistopis]
tags: [work, legislativa, stavebni-zakon]
---

# Stavební zákon (tisk 67) — tři vrstvy textu

## Co máš v ruce

**1. `cistopisy/67-00-CISTOPIS-1-puvodni-navrh.md`** — čistý text *původního* poslaneckého návrhu.
Vznikl z dokumentu „Platné znění s vyznačením navrhovaných změn" (t0067a0) odstraněním
přeškrtnutých (rušených) částí. Ukazuje, jak by znělo 41 dotčených zákonů (stavební zákon
283/2021 + 40 souvisejících) po přijetí původního návrhu — bez KPN a bez PN. Spolehlivé,
mechanické. Slouží jako referenční základna.

**2. `cistopisy/67-00-CISTOPIS-2-po-KPN-a-PN.md`** — **plný text zákona** po zapracování komplexního
pozměňovacího návrhu (KPN z 16. 4. 2026), s vyznačením individuálních PN.
- Čteš **souvislé znění zákona** (ne seznam pokynů).
- Logika: základem je čistopis #1; na něj se aplikuje KPN. Kde KPN nařizuje změnu, kterou
  původní návrh už udělal stejně, text se ponechá (změna už je v textu). Kde KPN přidává nebo
  mění nad rámec (nové paragrafy, přepsané odstavce), zapracuje se do textu.
- Paragrafy, které KPN změnil, nesou značku `[KPN čl./bod]`.
- **Modře orámované vsuvky** u paragrafu ukazují, co dál mění jednotlivé PN, značka `[PN číslo]`.
  Kde se o stejný paragraf uchází více návrhů, jsou uvedeny jako **kolize variant**
  (např. § 39a/39b — vzdálenost větrných elektráren: sedm návrhů od 1 500 m do 10 000 m).
- PN mířící na zákony mimo původní návrh (586/1992 daně z příjmů, 222/1999 obrana, 128/2000
  obce ad.) jsou v **příloze pod `---`**.

**3. `cistopisy/67-00-CISTOPIS-3-plne-nahrady-ze-272.md`** — vytěžené **plné náhrady**
ze senátního tisku 272/0. Oficiální text pro Senát je změnový, ne paragrafový celek.
Parser (`scripts/parse_senat272_zmenove.py`) z něj udělá mapu operací
(`PSP-podklady/senat-272/INDEX-zmenove-zneni.md`, `_operace-272.csv`)
a sem uloží jen bloky, kde bod říká „§ X zní:“ / „vkládají se nové § … které znějí:“.
To je čitelná vrstva pro klíčové nové paragrafy (§ 1a, 1b, soustava ÚRÚ…).
**Není to úplné znění zákona.** Slovní delty dávají smysl jen nad aktuální Sbírkou.

**4–6.** Základ e-Sbírky (`67-00-ZAKLAD-e-sbirka-2026-06-11.md`), konsolidát #4 (`~~zrušeno~~` / `**nově**`) a deltový výpis #5 — viz `CHANGELOG.md` a `VALIDACE-konsolidace-272.md`.

Od **2026-09-08** je čistopis #4 i čistopisy vedlejších zákonů generuje **engine v2**:
`base_tree.py` (strom § / odstavců / písmen / bodů **včetně příloh**) → `ops272.py`
(parser novelizačních instrukcí) → `merge_272_v2.py` (283/2021) a
`merge_272_laws_v2.py` (55 vedlejších zákonů). Starý `merge_272_annotated.py`
a `merge_272_laws.py` zůstávají jen pro srovnání; **negeneruj z nich**.

### Proč vznikla verze 2

Kontrola verze 1 proti 272/0 našla systémové vady, ne jednotlivé překlepy:

| Vada | Dopad |
|------|-------|
| Základ vůbec nenačítal **obsah příloh** (nemají fragment `Paragraf`) | 101 operací nemělo kam sáhnout; přílohy č. 1–3 (drobné/jednoduché/vyhrazené stavby) byly ve výstupu prázdné |
| Nenačítaly se nadpisy částí, hlav a dílů | 111 nadpisů chybělo |
| Rušení celých §, odstavců a písmen se neprovádělo | § 32a, 32b a 262 stály ve výstupu jako platné |
| „Na konci **textu** … se doplňují slova“ | text se lepil za tečku (`…opatření., a ve věcech…`) |
| Citace s mezerou na kraji (`„ , slova“`) | 76 operací se nedohledalo |
| Instrukce v `_operace-272.csv` **uříznuté na 400 znaků** | 99 z 735 operací u SZ (296 z 1628 celkem) — engine v2 čte plný text bodu z PDF |
| Dva články navěšené na špatný zákon (`RE_LAW` neuměl 7. pád) | Čl. LVII mířil na 217/2005 místo na 634/2004 |
| Vícecílové instrukce (`písm. d) a e)`), cílení na věty a písmena | měnil se jen první výskyt |
| Diff byl blokový | celý odstavec dvakrát; teď slovní (inline) diff |

Měřeno nezávisle (postpodmínka každé instrukce ověřená v cílovém uzlu):
**72 % → 96 %** splněných u jednoznačně měřitelných instrukcí.

## Co musíš vědět (bez vaty)

- **Není to právně závazný text.** KPN má přes 2 300 zásahů a přepisuje skoro celý návrh.
  Konsolidaci nelze stoprocentně zaručit. Před jednáním ověř konkrétní paragraf proti originálu.
- **Poznámky `⚠️ text nenalezen`** (cca 56×) označují místa, kde zásah KPN nešlo spolehlivě
  umístit do textu — buď proto, že původní návrh už použil jiné znění, nebo že poslanec míří na
  jiné znění či předložil zmetek. Stojí za prověření; v těch paragrafech text odpovídá původnímu
  návrhu, ne nutně znění KPN.
- **Drobné divergence se slovní vsuvkou** (kde KPN přidává pár slov k tomu, co návrh 67 už vložil)
  engine raději vynechá, aby nevznikla duplicita. Podstata (nové a přepsané paragrafy) je zapracovaná.

## Kolize k rozhodnutí (kde se návrhy perou o stejné místo)

- **§ 39a/39b — vzdálenost větrných elektráren:** PN 1025–1032, rozptyl 1 500–10 000 m. Nejcitlivější.
- **§ 12/§ 13 — přístupnost staveb / pojmy:** PN 596 vs PN 942.
- **§ 22 — archeologický výzkum:** PN 1114 vs PN 942.
- **§ 27/§ 54 — pravomoci obce / akcelerační oblasti:** PN 1019, PN 294 vs PN 942.
- **§ 47/§ 49 (DPH, energetika):** PN 531, 1055.
- **daň z nemovitých věcí (338/1992) a daň z příjmů (586/1992):** PN 1109, 1110 (mimořádné odpočty).

## Jak to vygenerovat znovu (když přibydou PN)

Skripty jsou ve `scripts/cistopis/` (Python + `lxml`). Pořadí:

1. `cistopis1.py` — z t0067a0 vytvoří čistopis #1.
2. `kpn_lib.py` — parser KPN (článek → zákon → body, plné texty vs slovní delty).
3. `pn_lib.py` — parser jednotlivých PN (plný text, přiřazení zákona přes mapu článků KPN).
4. `merge_engine.py` — aplikuje KPN na čistopis #1 (plné texty nahradí, delty bezpečně provede).
5. `build_cistopis2.py` — sestaví finální čistopis #2 (plný text + PN vsuvky + příloha).

6. `scripts/parse_senat272_zmenove.py` — ze senátního tisku 272/0 udělá index změnového znění a čistopis #3 (plné náhrady).

### Čistopis #4 a vedlejší zákony (engine v2)

```
python scripts/cistopis/merge_272_v2.py         # 283/2021 -> čistopis #4 + #5 + validace
python scripts/cistopis/merge_272_laws_v2.py    # 55 vedlejších zákonů -> cistopisy/272/
python scripts/cistopis/merge_272_laws_v2.py --law 114/1992   # jen jeden zákon
```

Engine nic nezahazuje mlčky: co neumí, vypíše do
`cistopisy/VALIDACE-konsolidace-272.md` a `cistopisy/VALIDACE-272-ostatni.md`
jako **neaplikované body k ruční kontrole**.

Stav k 2026-09-08:

| | Operací | Aplikováno | K ruční kontrole |
|---|---|---|---|
| 283/2021 (čistopis #4) | 735 | 732 | **3** |
| 55 vedlejších zákonů | 889 | 777 | **87** |

Z 87 nedodělků u vedlejších zákonů je **67 zásahů do tabulek** (sazebník
správních poplatků 634/2004, kategorie a sloupce příloh 100/2001) — e-Sbírka
je vydává jako `[tabulka]` a textově se adresovat nedají. Dalších 7 jsou
novelizace jiných novel („V části páté čl. VII bodě 2…“). Zbývá 13 běžných
zásahů — ty ověř ručně.

Pozn.: prostředí občas vkládá do .py souborů „null byty"; před spuštěním je vyčisti
(`tr -d '\000' < soubor.py > x && mv x soubor.py`).
