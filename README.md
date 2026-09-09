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

## Účinnost — barevné rozlišení

Novela nabývá účinnosti po částech (Čl. LXXXV tisku 272/0). V prohlížeči je
u každého dotčeného ustanovení barevný pruh u levého okraje a štítek s datem;
po najetí myší se ukáže celé pravidlo. V panelu nad textem jde podle účinnosti
filtrovat.

| Barva | Účinnost | Pravidlo |
|---|---|---|
| žlutá | **1. 1. 2027** | obecné pravidlo — vše, co nespadá pod písm. a) ani b) |
| červená | **prvním dnem měsíce po vyhlášení** | Čl. LXXXV písm. a) |
| zelená | **1. 1. 2028** | Čl. LXXXV písm. b) |

Zařazení se odvozuje z čísla novelizačního bodu, které je u každého ustanovení
uvedené v hranaté závorce (`[272 Čl.I/12]`). Ustanovení dotčené více body může
mít víc kategorií najednou.

Pozn.: červená a zelená *uvnitř* textu znamenají něco jiného — škrtnutý
(rušený) a tučný (nový) text. Účinnost se proto značí okrajem, ne barvou písma.

## Jak čistopisy vznikly

Základem je **aktuálně účinné znění z e-Sbírky**; na něj se strojově aplikují
novelizační body ze senátního tisku 272/0 v pořadí, v jakém je tisk uvádí
(včetně přečíslování odstavců a písmen po vložení či zrušení).

Stav zapracování:

| | Operací | Aplikováno | K ruční kontrole |
|---|---|---|---|
| 283/2021 Sb. | 735 | 732 | 3 |
| 55 souvisejících zákonů | 889 | 775 | 89 |

Znění je porovnané s **oficiálním pracovním čistopisem MMR**
(„Aktuální podoba znění stavebního zákona… verze pro projednání v Senátu",
srpen 2026). Průměrná shoda 97,7 %; 88 % paragrafů se shoduje nad 95 %.
Porovnání odhalilo, že tisk ruší devět paragrafů strukturálně (zrušením
celého dílu či oddílu) — §§ 44, 45, 106, 107, 136a, 201, 202, 216 a 217.

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
