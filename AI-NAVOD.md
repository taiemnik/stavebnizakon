# Jak se ptát svého AI asistenta na novelu stavebního zákona

Tahle sbírka je připravená tak, aby si ji kdokoli mohl dát svému AI asistentovi (ChatGPT, Claude, Gemini, Copilot, NotebookLM…) a ptát se ho vlastními slovy. AI odpovídá jen tak dobře, jak dobré má podklady a pokyny – proto je níže připravený obojí.

## 1. Dejte AI podklady

Vyberte si jednu z cest:

- **Nejjednodušší – balík souborů.** Stáhněte [stavebni-zakon-2026-pro-ai.zip](https://taiemnik.github.io/stavebnizakon/ai/stavebni-zakon-2026-pro-ai.zip) (1,7 MB), rozbalte ho a soubory nahrajte do chatu, do projektu nebo do NotebookLM jako zdroje. Balík obsahuje přehled novinek, rejstřík změn, znění zákona před novelou a po ní, účinnost a přechodná ustanovení, úřední text novely, stenozáznamy rozprav, hlasování a katalog všech zdrojů s odkazy.
- **Připojení GitHubu.** Pokud váš nástroj umí připojit repozitář GitHub (například ChatGPT nebo Claude přes konektor GitHub), připojte veřejné repo `taiemnik/stavebnizakon`.
- **Odkaz na web.** Nástroje, které umí číst web, nasměrujte na [https://taiemnik.github.io/stavebnizakon/llms.txt](https://taiemnik.github.io/stavebnizakon/llms.txt) – je to rozcestník souborů psaný přímo pro AI.
- **Vývojáři:** `git clone https://github.com/taiemnik/stavebnizakon.git` – všechny texty jsou v Markdownu, metadata v `katalog.json`.

Tip: konsolidované znění stavebního zákona má přes 600 kB a do kontextu menších modelů se nemusí vejít. Pak použijte rejstřík změn `cistopis/info/283-2021-rejstrik-zmen.md`, výtah `cistopis/info/283-2021-jen-zmeny.md` nebo NotebookLM, který s velkými zdroji pracuje dobře.

## 2. Vložte AI tento pokyn

Zkopírujte ho na začátek konverzace nebo do instrukcí projektu (Claude Projects, ChatGPT Projects, Gemini Gem). Pokyn má 2 664 znaků, do „vlastních instrukcí“ ChatGPT s limitem 1 500 znaků se nevejde.

```text
Jsi pomocník pro orientaci v novele stavebního zákona 2026 (sněmovní tisk 67, senátní tisk 272; mění zákon č. 283/2021 Sb. a 55 dalších zákonů). Odpovídáš z podkladů ve sbírce https://github.com/taiemnik/stavebnizakon nebo ze souborů, které ti nahraji. Začni souborem CO-JE-NOVEHO.md.

Podklady podle váhy:
1. Zákon. cistopis/283-2021.md je znění po novele (rušený text ~~přeškrtnutý~~, nový **tučně**, {uc=…} = účinnost), cistopis/info/283-2021-pred-novelou-2026-06-11.md je dnešní znění. Co se mění, zjistíš jejich porovnáním; seznam změněných paragrafů je v cistopis/info/283-2021-rejstrik-zmen.md. Ostatní zákony: cistopis/<číslo>-<rok>.md.
2. Úřední text novely: zdroje/senat/tisky/272-0-navrh-zakona.md. Účinnost a přechodná ustanovení (rozběhnutá řízení, přechod úřadů a zaměstnanců na stát) nejsou v textu stavebního zákona, ale v samotné novele, tedy ve změnovém zákoně (Čl. II a Čl. LXXXV): cistopis/_ucinnost.md.
3. Souvislosti: stenozáznamy rozprav, usnesení a pozměňovací návrhy (zdroje/psp, zdroje/senat). Důvodová zpráva v tisku 67/0 patří k původnímu návrhu, který komplexní pozměňovací návrh z velké části přepsal – jako vysvětlení ji použij jen tam, kde se text nezměnil, a řekni to.
4. Výklady a názory: weby a metodiky MMR, stanoviska institucí, články (KATALOG.md). Máš k nim jen krátký popis, ne text. Podrobnosti z popisu neodvozuj; řekni, kdo co tvrdí, a doporuč přečíst originál (odkaz je u popisu).

Dvě nejčastější otázky:
A) „Co je nového?“ Nejdřív stav legislativního procesu a nejbližší termín (CO-JE-NOVEHO.md), pak hlavní změny zákona podle rejstříku změn, seskupené podle témat. Vlastní hodnocení, jestli je změna dobrá, nepřidávej.
B) „Jak se mě to týká?“ Nejdřív zjisti, kdo se ptá (vlastník pozemku, stavebník, soused, obec, úředník…) a o jakou situaci jde (druh a velikost stavby, rozběhnuté řízení). Pak odpověz v pořadí: co platí dnes → co bude platit po novele → od kdy → co z toho plyne → co si ověřit. Vždy s paragrafy obou znění.

Pravidla:
- U každého věcného tvrzení uveď zdroj: zákon a paragraf (např. „§ 170 zákona č. 283/2021 Sb. ve znění novely“) nebo dokument a místo v něm.
- Konsolidované znění je strojově sestavená pracovní pomůcka, ne úřední text. Do vyhlášení ve Sbírce zákonů je úředním textem senátní tisk 272/0, potom znění ve Sbírce.
- Když odpověď v podkladech není nebo si nejsi jistý, řekni to otevřeně. Nic si nedomýšlej a nevydávej odhad za fakt.
- Piš srozumitelně pro člověka bez právního vzdělání: nejdřív krátká odpověď (2–4 věty), pak podrobnosti a zdroje.
- U konkrétní stavby, pozemku nebo řízení doporuč ověření na příslušném stavebním úřadě nebo u advokáta – tvoje odpověď není právní rada.
```

## 3. Dvě nejčastější otázky

### Co je nového?

AI začne souborem `CO-JE-NOVEHO.md`: kde je zákon v legislativním procesu, co nastane příště a co ve sbírce nově přibylo. Pak projde rejstřík změněných paragrafů.

- Co je nového v novele stavebního zákona? Kde je teď legislativní proces a jaký je nejbližší termín?
- Jaké jsou hlavní změny stavebního zákona? Seskup je podle témat a u každé uveď paragraf a od kdy platí.
- Co se změnilo od schválení ve Sněmovně v červenci 2026?

### Jak se mě to týká?

Napište, kdo jste a o jakou situaci jde – čím konkrétněji, tím lepší odpověď:

```text
Jsem [vlastník pozemku / stavebník / soused stavby / starosta obce / úředník stavebního úřadu].
[Popište situaci: co chcete postavit nebo změnit, jak velké, kde, jestli už běží řízení.]
Jak se mě novela týká? Co platí dnes, co bude platit po novele, od kdy a co mám udělat?
```

Příklady:

- Mám pozemek a chci na něm postavit garáž 40 m². Co k tomu budu potřebovat po 1. 1. 2027 a co dnes?
- Soused bude stavět bytový dům. Jak a v jaké lhůtě se můžu k řízení vyjádřit po novele?
- Mám rozběhnuté stavební řízení. Podle jakých pravidel se dokončí?
- Jsem starosta obce, která pořizuje územní plán. Co se pro nás mění a od kdy?
- Pracuji na obecním stavebním úřadě. Co se stane s mým pracovním poměrem k 1. 1. 2028?

Na konci se AI vždy zeptejte: **„Z jakých souborů a paragrafů jsi vycházel?“** a důležité věci si ověřte v uvedeném zdroji.

## 4. Další otázky

- Co je fikce souhlasu nebo fikce povolení a kdy nastane?
- Které stavby bude povolovat Úřad rozvoje území a které zůstanou úřadům v území?
- Jaké argumenty zazněly v Senátu proti novele a jak na ně reagovalo ministerstvo?

## Kde co je

| Otázka | Kde AI hledá |
|---|---|
| Kde je zákon v procesu, co je nového | `CO-JE-NOVEHO.md` |
| Které paragrafy se mění a od kdy | `cistopis/info/283-2021-rejstrik-zmen.md` |
| Jak paragraf zní dnes a po novele | `cistopis/info/283-2021-pred-novelou-2026-06-11.md`, `cistopis/283-2021.md` |
| Od kdy co platí, rozběhnutá řízení, přechod úřadů a zaměstnanců | `cistopis/_ucinnost.md` (přechodná ustanovení novely) |
| Úřední text novely | `zdroje/senat/tisky/272-0-navrh-zakona.md` |
| Proč to zákonodárci chtěli, jaké padly argumenty | stenozáznamy v `zdroje/psp/stenozaznamy/` a `zdroje/senat/stenozaznamy/` |
| Co říká ministerstvo, komory, svazy, média | `KATALOG.md` – jen krátký popis a odkaz, originál si přečtěte sami |

## Na co dát pozor

- **Konsolidované znění je pracovní pomůcka**, ne úřední text. Závazné bude znění vyhlášené ve Sbírce zákonů.
- **AI se může mýlit** – i s dobrými podklady si někdy „domyslí“ odpověď. Proto chtějte zdroje.
- **Názory nejsou zákon.** Stanoviska, články a projevy v parlamentu jsou pohledy konkrétních lidí; zákon říká jen to, co je v jeho textu.
- **Stanoviska a metodiky čtěte v originálu.** Sbírka k nim má jen krátký popis a odkaz; AI z popisu nezná podrobnosti.
- **U konkrétní věci** (vaše stavba, pozemek, řízení) se obraťte na stavební úřad nebo advokáta.
