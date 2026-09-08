# Validace konsolidace 272/0 nad e-Sbírkou (engine v2)

> Přegenerováno: 2026-09-04 · Základ: [https://e-sbirka.gov.cz/sb/2021/283/2026-06-11?f=283%2F2021&zalozka=text](https://e-sbirka.gov.cz/sb/2021/283/2026-06-11?f=283%2F2021&zalozka=text)
> Skript: `scripts/cistopis/merge_272_v2.py` (base_tree + ops272)

## Souhrn

| Metrika | Počet |
|---------|-------|
| Operací 283/2021 v CSV | 735 |
| Aplikováno | 732 |
| Neaplikováno (engine neumí) | 3 |
| Dílčích akcí: už zapracováno dřívějším bodem | 11 |
| Dílčích akcí: cíl nalezen, text nesedí | 20 |
| Přechodná ustanovení (Čl. II) | 1 |
| Změněných bloků v čistopisu | 1133 |

| § v základě | 341 |
| § po konsolidaci | 346 |
| Nových § | 47 |
| Zrušených § | 42 |
| Změněných uzlů v přílohách | 188 |

## Zrušené paragrafy

§ 16, § 17, § 19, § 20, § 23, § 25, § 26, § 28, § 29, § 30, § 30a, § 31, § 32, § 32a, § 32b, § 33, § 34, § 34a, § 37, § 43, § 46, § 47, § 48, § 55, § 59, § 66, § 91, § 94, § 99, § 117, § 176, § 179a, § 214, § 226, § 243, § 244, § 246, § 260, § 262, § 298, § 308, § 309

## Nové paragrafy

§ 1a, § 1b, § 16, § 17, § 17a, § 17b, § 19, § 20, § 23, § 25, § 26, § 28, § 30, § 31, § 32, § 33, § 34, § 37, § 39a, § 43, § 46, § 47, § 55, § 59, § 111a, § 115a, § 117, § 144b, § 144c, § 144d, § 152a, § 176, § 179a, § 190a, § 191a, § 194, § 194a, § 195a, § 195b, § 200a, § 212a, § 226, § 246, § 298, § 308, § 308a, § 309

## Neaplikované body — vyžadují ruční kontrolu

| Bod | Typ | Instrukce |
|---|---|---|
| 272 Čl.I/290 |  | V části třetí hlavě III dílu 5 se označení oddílu 3 včetně nadpisu nahrazuje označením dílu 6, které včetně nadpisu zní: „Díl 6 Nezastavitelné území“. |
| 272 Čl.I/354 |  | V § 157 odst. 1 písm. d) se za slova „provádění stavby,“ vkládají slova „jednoduchých staveb bytových domů uvedených v odstavci 1 písm. b) přílohy č.  |
| 272 Čl.I/356 |  | V § 157 odst. 1 písm. e) se za slova „odstranění stavby,“ vkládají slova „jednoduchých staveb bytových domů uvedených v odstavci 1 písm. b) přílohy č. |

## Dílčí akce, kde text nesedí

| Bod | Akce | Detail |
|---|---|---|
| 272 Čl.I/28 | zruseni | body 1 a 2 se zrušují |
| 272 Čl.I/28 | zruseni | body 1 a 2 se zrušují |
| 272 Čl.I/148 | nahrazeni | slova „ , kdy schválil možnost jejího využití,“ se nahrazují slovy „jejího schválení vložením“ |
| 272 Čl.I/167 | ? | se slova „zastavitelné plochy, transformační“ |
| 272 Čl.I/167 | ? | slova „dopravní a technické infrastruktury“ |
| 272 Čl.I/283 | zruseni_pismene | písmeno d) se zrušuje |
| 272 Čl.I/354 | vlozeni_za | se za slova „provádění stavby,“ vkládají slova „jednoduchých staveb bytových domů uvedených v odstav |
| 272 Čl.I/356 | vlozeni_za | se za slova „odstranění stavby,“ vkládají slova „jednoduchých staveb bytových domů uvedených v odsta |
| 272 Čl.I/455 | nahrazeni | věta poslední se nahrazuje větami „Toto oznámení potvrzuje soulad dokumentace pro povolení stavby s  |
| 272 Čl.I/554 | vlozeni_za | ve větě druhé se za slovo „vznikla“ vkládá slovo „povinnému,“ |
| 272 Čl.I/568 | zruseni_pismene | písmeno d) se zrušuje |
| 272 Čl.I/580 | ? | se slova „opakovaně nebo“ |
| 272 Čl.I/639 | nahrazeni | číslo „8“ se nahrazuje číslem „4“ |
| 272 Čl.I/656 | ? | slova „ , jehož distribuční soustava je připojena k přenosové soustavě a k jehož soustavě je připoje |
| 272 Čl.I/657 | ? | slova „ , k jehož soustavě je připojeno více než 90 000 odběrných míst,“ |
| 272 Čl.I/690 | ? | se dosavadní text označuje jako odstavec 1 |
| 272 Čl.I/719 | ? | se slova „ , transformačních ploch“ |
| 272 Čl.I/723 | ? | se slovo „vymezení“ |
| 272 Čl.I/723 | ? | slova „územního systému ekologické stability a vymezení“ |
| 272 Čl.I/739 | ? | se slova „ , které jsou součástí“ |

## Co engine v2 opravil proti v1

- přílohy č. 1–9 se do základu vůbec nenačítaly → 101 operací nemělo kam sáhnout
- rušení celých §, odstavců a písmen se neprovádělo (§ 32a, 32b, 262 zůstávaly jako platné)
- „na konci textu … se doplňují slova“ vkládalo text za tečku místo před ni
- citace s mezerou na kraji („ , slova“) se nedohledaly — 76 operací
- vícecílové instrukce měnily jen první výskyt
- cílení na věty a písmena se ignorovalo
- diff byl blokový (celý odstavec 2×), teď je slovní

## Verdikt

Pracovní konsolidát nad e-Sbírkou 2026-06-11. **Není** to právně závazný text
ani náhrada Sbírkového znění po vyhlášení. Body v tabulkách výše ověř ručně
proti `PSP-podklady/senat-272/ST_272.pdf`.
