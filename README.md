# Stavební zákon — novela 2026 (sněmovní tisk 67 / senátní tisk 272)

Konsolidovaná („úplná") znění stavebního zákona a souvisejících předpisů se
zapracovaným senátním tiskem **272/0**, plus veřejné podklady k legislativnímu procesu.

**Prohlížeč:** https://taiemnik.github.io/stavebnizakon/cistopis.html

## Co tu je

| Složka | Obsah |
|---|---|
| `cistopisy/` | Konsolidovaná znění. Rušený text ~~škrtnutý~~, nový **tučně** (slovní diff). |
| `cistopisy/272/` | Jeden soubor na zákon — 283/2021 celý, 55 souvisejících zákonů jen v dotčených ustanoveních. |
| `podklady/senat-272/` | Senátní tisk 272 (včetně výborových tisků) a veřejná stanoviska — ČKAIT, ČKA, SMS ČR. |
| `podklady/snemovni-tisky/` | Sněmovní tisk 67 a stanovisko vlády. |
| `podklady/pozmenovaci-navrhy/` | Pozměňovací návrhy podané ve Sněmovně. |
| `podklady/stenozaznamy/` | Stenozáznamy z rozpravy PSP a Senátu. |
| `zdroje/` | Přepisy veřejného podcastu MMR „Stavíme na faktech". |

## Jak čistopisy vznikly

Základem je **aktuálně účinné znění z e-Sbírky**; na něj se strojově aplikují
novelizační body ze senátního tisku 272/0 v pořadí, v jakém je tisk uvádí
(včetně přečíslování odstavců a písmen po vložení či zrušení).

Stav zapracování:

| | Operací | Aplikováno | K ruční kontrole |
|---|---|---|---|
| 283/2021 Sb. | 735 | 732 | 3 |
| 55 souvisejících zákonů | 889 | 775 | 89 |

Většina nezapracovaných bodů jsou zásahy do **tabulek** (sazebník správních
poplatků, kategorie příloh zákona o posuzování vlivů) — e-Sbírka je vydává bez
struktury, takže je nelze adresovat textově. Nic se nezahazuje mlčky: každý
nezapracovaný bod je vypsaný v `cistopisy/VALIDACE-*.md` a v souboru
příslušného zákona pod nadpisem „Nezapracované novelizační body".

## Limity

**Není to právně závazný text.** Je to pracovní pomůcka pro orientaci v tom, co
se mění. Před závazným použitím ověř konkrétní ustanovení proti
`podklady/senat-272/ST_272.pdf` a proti platnému znění v e-Sbírce.

Senát tisk **20. 8. 2026 zamítl**; návrh se vrací do Sněmovny, která ho může
přehlasovat 101 hlasy. Do vyhlášení ve Sbírce jde tedy o návrh, ne o platné právo.
