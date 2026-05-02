# Contributing to Forum Hungaricum · Hozzájárulási útmutató

Köszönjük az érdeklődésed a Forum Hungaricum iránt. Ez egy közérdekű civic-tech projekt, és tudományosan, szakmailag, valamint közösségi szempontból is értékeljük a hozzájárulásokat.

Thank you for your interest in Forum Hungaricum. This is a civic-tech public-interest project, and we value contributions on academic, professional, and community levels.

---

## Áttekintés · Overview

A Forum Hungaricum **nem hagyományos open-source projekt** — **stratégiai átláthatóság** elvét követi:

- **Adat és módszertan = nyílt** (CC BY-SA / CC0 / MIT licenc, nyilvános repo)
- **Platform-kód, AI-modellek, infrastruktúra = proprietary** (privát repo, nem hozzáférhető külső contributoroknak)

Ennek megfelelően a hozzájárulások **típus szerint** különböző csatornákon érkeznek be.

Forum Hungaricum is **not a traditional open-source project** — it follows a **strategic transparency** principle:

- **Data and methodology = open** (CC BY-SA / CC0 / MIT licensed, public repos)
- **Platform code, AI models, infrastructure = proprietary** (private repos, not accessible to external contributors)

Accordingly, contributions arrive through **different channels by type**.

---

## Hozzájárulási csatornák · Contribution channels

### 1. Módszertan és validáció · Methodology & validation
**Repo**: `forum-hungaricum/methodology` (CC BY-SA 4.0)
**Hogyan / How**: Issue + Pull Request a megfelelő `methodology/` szakaszhoz. Példák: új validation rule, jogi státusz-átmenet logika finomítása, új CRI-feature javaslat.

### 2. Adat-hozzájárulás · Data contribution
**Repo**: `forum-hungaricum/data` (CC BY-SA 4.0 / CC0)
**Hogyan / How**: Strukturált adat új entitásokról, ügyekről, kapcsolatokról — minden mező mellett **forrás-link** és **forrás-osztály-jelölő**. Lásd a `CONTRIBUTING-DATA.md` szakaszos sablont a repo-ban.

⚠️ **Fontos**: nem-megerősített állítások (csak egy sajtó-forrás) NEM kerülnek a fő `data/` ágba — `pending/` mappába, ahol a Reviewer-ágens feldolgozza.

### 3. Schema és API · Schema & API
**Repo**: `forum-hungaricum/schema-public`, `forum-hungaricum/api-docs` (MIT)
**Hogyan / How**: Issue / PR. Példa: új entity-attribútum-javaslat, API-pattern-javítás, OpenAPI-spec finomítás.

### 4. Civic-érték scraperek · Civic-value scrapers
**Repo**: `forum-hungaricum/scrapers-civic` (MIT)
**Hogyan / How**: Új scraper magyar nyilvános adatforrásokra (Magyar Közlöny, Bírósági Határozatok Gyűjteménye, EKR), respect-rate-limit, polite User-Agent, robots.txt-tisztelő.

### 5. Anonim adat / sztori-tipp · Anonymous data / story tips
**NEM GitHub-on**, hanem a publikus platform anonim intake-csatornáján (Tabella) keresztül, Tor-on és clearneten egyaránt elérhető.

**NOT through GitHub** — use the platform's anonymous intake (Tabella), available via Tor and clearnet.

[Kezdő-link a publikus intake-re hamarosan / Starter link to public intake coming soon]

### 6. Sajtói-szerkesztőségi együttműködés · Press-newsroom collaboration
**Csatorna**: [press@forumhungaricum.eu](mailto:press@forumhungaricum.eu)
Magyar és nemzetközi szerkesztőségek embargós sztori-cseréje, közös-kutatási dossziék, API-szintű integráció.

### 7. Anyagi támogatás · Financial support
A platform **közönség-által-fizetett**: 1% adófelajánlás, Patreon, Open Collective, egyedi adományok. Részletek a publikus weboldalon.

The platform is **community-funded**: Hungarian 1% tax allocation, Patreon, Open Collective, individual donations. Details on the public website.

---

## Pull Request folyamat · Pull Request process

### Repo-szintű
1. **Fork**-old a megfelelő publikus repo-t
2. **Branch**-elj: `git checkout -b descriptive-name`
3. **Commit**-eld a változtatásaidat (világos commit message)
4. **Push**-old a forkodra
5. **Nyiss egy Pull Request**-et a `main` ágra
6. Egy maintainer **review**-ozza, Code of Conduct + technikai szempontok szerint

### Code style és docs style
- **Kód**: a megfelelő nyelvi standard (PEP 8 Pythonra, ESLint TypeScriptre)
- **Docs**: jelölt nyelv (HU vagy EN) konzisztens egy fájlon belül; ha kétnyelvű, mindkét rész teljes
- **Commit-üzenet**: Conventional Commits — `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`

### Review-kritériumok
- **Forrás-link minden új tényadatra**
- **Forrás-osztály-jelölő** kötelező
- **Magyar és angol konzisztencia** dokumentumokban
- **Jogi-eljárási státusz** mindig dátumozva és forrás-linkelve
- **Right-of-reply** jegyzék minden új profil/ügy mellett

---

## Mit NEM kérünk · What we don't accept

- **Nem-megerősített állítások** valós nevekkel (csak egy sajtó-forrás, "valaki valahol írt erről") — ezek a `pending/` mappába kerülnek vagy az anonim intake-en jönnek be
- **Politikai retorika** — szakmai tartalmi viták üdvözöltek, partizán-állásfoglalás nem
- **Spam, harassment, doxxing** — lásd `CODE_OF_CONDUCT.md`
- **Privát infrastruktúra-érzékeny információ** publikus repóban (deployment configok, kulcsok, API-tokenek)

---

## Nyelv-irányelv · Language policy

A projekt **kétnyelvű** (magyar + angol). Néhány fájl elsősorban magyarul (`docs/hu/...`), néhány elsősorban angolul (`docs/en/...`), és pár dokumentum kétnyelvű egyetlen fájlban (mint ez).

Tippek:
- **Methodology whitepaper**: angol az elsődleges (nemzetközi sajtó és akadémia ezt olvassa); magyar fordítás külön
- **Adat-mezők**: technikai mezőnevek angolul (pl. `procurement_value_huf`); a tartalom magyarul, ahogy a forrás szerepel
- **Issue/PR**: bármelyik nyelven, de **válaszadás** annak nyelvén, amelyiken írtad

The project is **bilingual** (Hungarian + English). Some files are primarily Hungarian, some primarily English, some bilingual in one file.

Tips:
- **Methodology whitepaper**: English primary (international press and academia read this); Hungarian translation separate
- **Data fields**: technical field names in English (e.g., `procurement_value_huf`); content in original language as in source
- **Issue/PR**: any language, but **response** in the language you used

---

## Etikai kódex és viselkedés · Ethics and behavior

Lásd / See: [`CODE_OF_CONDUCT.md`](./CODE_OF_CONDUCT.md)

Speciális kiegészítés a Forum Hungaricum-hoz: a projekt **apolitikus a műfaj természeténél fogva**, és minden kormányzati ciklust egyformán dokumentál. Pártpolitikai aktivizmus a projekt-csatornákon nem üdvözölt.

---

## Kapcsolat · Contact

- **Általános kérdések / General**: [kontakt@forumhungaricum.eu](mailto:kontakt@forumhungaricum.eu)
- **Sajtó / Press**: [press@forumhungaricum.eu](mailto:press@forumhungaricum.eu)
- **Sebezhetőség / Security**: [security@forumhungaricum.eu](mailto:security@forumhungaricum.eu) — lásd / see [`SECURITY.md`](./SECURITY.md)
- **Jogi kérdések / Legal**: [legal@forumhungaricum.eu](mailto:legal@forumhungaricum.eu)

---

*Last updated: 2026-05-02*
