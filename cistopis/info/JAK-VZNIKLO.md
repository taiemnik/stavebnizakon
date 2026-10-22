# Jak konsolidované znění vzniklo a co neumí

Konsolidované („úplné“) znění ve složce `cistopis/` ukazuje, jak budou zákony vypadat po novele. Není to úřední text. Je to pracovní pomůcka, kterou sestavil Josef Procházka, aby se dalo číst souvislé znění místo stovek novelizačních pokynů.

## Z čeho se skládá

- **Základ:** aktuálně účinné znění zákonů z [e-Sbírky](https://e-sbirka.gov.cz/) ke dni **11. 6. 2026**.
- **Změny:** novelizační body ze **senátního tisku 272/0**, tedy ze znění, které Sněmovna schválila 10. 7. 2026 a na němž 9. 9. 2026 setrvala. Body se aplikují strojově v pořadí, v jakém je tisk uvádí, včetně přečíslování odstavců a písmen po vložení či zrušení.
- **Rozsah:** zákon č. 283/2021 Sb. (stavební zákon) celý; dalších 55 zákonů jen v ustanoveních, kterých se novela dotýká. Celkem 1 628 novelizačních operací.

## Jak číst vyznačení

- ~~přeškrtnutý text~~ = ruší se, **tučný text** = nový. Diff je slovní, ne celé odstavce.
- U ustanovení je v hranaté závorce číslo novelizačního bodu, např. `[272 Čl.I/12]` = Čl. I bod 12 senátního tisku 272/0.
- Značka `{uc=A}`, `{uc=B}`, `{uc=C}` určuje účinnost (v prohlížeči barevný pruh u levého okraje):

| Značka | Barva v prohlížeči | Účinnost |
|---|---|---|
| A | žlutá | **1. 1. 2027** – obecné pravidlo Čl. LXXXV |
| B | červená | **prvním dnem měsíce po vyhlášení** – Čl. LXXXV písm. a) |
| C | zelená | **1. 1. 2028** – Čl. LXXXV písm. b) |

Účinnost a přechodná ustanovení novely (Čl. II, Čl. LXXXV a další) jsou v souboru [`cistopis/_ucinnost.md`](../_ucinnost.md). Ustanovení novely, která nemění žádný konkrétní zákon, jsou v [`cistopis/_bez-cisla.md`](../_bez-cisla.md).

## Kontrola

- **Stav zapracování** – stavební zákon: 735 operací, 732 aplikováno, 3 k ruční kontrole; 55 souvisejících zákonů: 889 operací, 89 k ruční kontrole. Podrobně v souborech `VALIDACE-*.md` v této složce.
- **Srovnání s pracovním zněním MMR** („Aktuální podoba znění stavebního zákona…, verze pro projednání v Senátu“, srpen 2026): průměrná shoda 97,7 %, 88 % paragrafů se shoduje nad 95 %. Srovnání odhalilo, že tisk ruší devět paragrafů strukturálně, zrušením celého dílu či oddílu (§§ 44, 45, 106, 107, 136a, 201, 202, 216 a 217).
- **Nic se nezahazuje mlčky.** Každý nezapracovaný bod je vypsaný ve validaci a v souboru příslušného zákona pod nadpisem „Nezapracované novelizační body“. Většinou jde o zásahy do **tabulek** (sazebník správních poplatků, kategorie příloh zákona o posuzování vlivů), které e-Sbírka vydává bez struktury, takže je nelze adresovat textově.

## Limity

- **Není to právně závazný text.** Před závazným použitím ověřte konkrétní ustanovení v senátním tisku 272/0 (`zdroje/senat/tisky/`) a po vyhlášení ve Sbírce zákonů.
- Základ je k 11. 6. 2026. Pokud se zákon mezitím změnil jinou novelou, tady to není.
- Po vyhlášení novely ve Sbírce zákonů se znění přegeneruje proti úřednímu textu.

Chybu nebo nesrovnalost prosím nahlaste přes [GitHub Issues](https://github.com/taiemnik/stavebnizakon/issues).
