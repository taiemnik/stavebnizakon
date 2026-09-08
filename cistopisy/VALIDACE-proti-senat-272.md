# Validace čistopisu #2 proti senátnímu tisku 272/0

> Provedeno: 2026-08-19 · Skript: `scripts/validace_proti_senat272.py`

## Kontext

Čistopis #2 (`cistopisy/67-00-CISTOPIS-2-po-KPN-a-PN.md`) vznikl automatickým
zapracováním KPN z **16. 4. 2026** a 25 individuálních PN do původního návrhu (tisk 67).
Senátní tisk 272/0 je **oficiální novelizační text** postoupený Senátu po schválení
Sněmovnou **10. 7. 2026** — tedy po třetím čtení, kde se hlasovalo o ~130 PN a garanční výbor osvojil jiný KPN (PN 1256
ze 27. 5. 2026).

**Očekávané zdroje rozdílů:**
- Vstupní KPN byl z 16. 4., ne z 27. 5. (nový KPN HV). Část rozdílů je tedy vysvětlitelná vstupem.
- Pipeline pracovala s 25 PN, hlasovalo se o ~130.
- 56 míst označených `⚠️ text nenalezen` (kde engine nemohl umístit zásah).
- PN vsuvky v čistopisu jsou označené, ne zapracované do textu.

## Verdikt

**Nedá se udělat přímý paragrafový diff.** Soubor `ST_272.pdf` není konsolidované
úplné znění stavebního zákona, ale **novelizační text** typu „v § X se mění...“.

### Co to znamená

- Přímé porovnání proti `67-00-CISTOPIS-2-po-KPN-a-PN.md` by bylo metodicky chybné.
- Nízké počty paragrafů v PDF nejsou důkaz, že čistopis je špatně; PDF prostě nemá stejný typ textu.
- Pro poctivou validaci je potřeba **konsolidované úplné znění** stavebního zákona po schválení novely,
  anebo znovu aplikovat přijaté změny nad aktuální Sbírkou.

### Dílčí verdikt

**Pipeline zatím nelze definitivně potvrdit ani vyvrátit tímto PDF.**
Tohle PDF je vhodné pro faktcheck jednotlivých změn, ale ne pro plný diff paragraf-po-paragrafu.

### Co už víme jistě

- Paragrafů v pracovním čistopisu: **425**
- Míst `text nenalezen`: **56**
- Čistopis zůstává pracovní artefakt a pro citace se používá oficiální novelizační text + následně konsolidované znění.
- **Praktická vrstva ze změnového znění (2026-08-20):** `PSP-podklady/senat-272/INDEX-zmenove-zneni.md` (1 628 operací, 85 článků, 259 stran) a `cistopisy/67-00-CISTOPIS-3-plne-nahrady-ze-272.md` (351 plných náhrad, z toho 148 u 283/2021). To pořád není konsolidovaný zákon — je to mapa + vytěžené přepisy.

---

*Generováno automaticky. Vstup: `67-00-CISTOPIS-2-po-KPN-a-PN.md` (425 §) vs. `ST_272.pdf` (0 §).*