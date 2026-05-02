# `.github` repo — Forum Hungaricum org-szintű setup

Ez a mappa a **`forum-hungaricum/.github`** privát repo-t reprezentálja. Bármi, ami ebben a mappában van, **az egész GitHub Organizationre automatikusan érvényes**.

A GitHub `.github` "magic" repo: ha egy organization létrehoz egy `.github` nevű repo-t, az abban lévő `profile/README.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md` fájlok **mind az összes repo-ra automatikusan érvényesek lesznek** alapértelmezésként, és a `profile/README.md` az **org publikus arca** lesz a `https://github.com/forum-hungaricum` oldalon.

---

## Tartalom

| Fájl | Cél |
|---|---|
| `profile/README.md` | A publikus org-arc (https://github.com/forum-hungaricum oldalon jelenik meg) |
| `SECURITY.md` | Sebezhetőség-bejelentési irányelv (RFC 9116-kompatibilis) |
| `CODE_OF_CONDUCT.md` | Magatartási kódex (Contributor Covenant 2.1 + apolitikus-by-genre kiegészítés) |
| `CONTRIBUTING.md` | Hozzájárulási útmutató (strategic transparency keretben) |

---

## Telepítés GitHub-on

### Opció A: GitHub web UI-on (egyszerűbb)

1. Menj `https://github.com/forum-hungaricum`
2. **New repository** → név: **`.github`** (pont-ponttal kezdődik!)
3. Visibility: **Public** (de a benne lévő tartalom amúgy is publikus, csak az ALAPÉRTELMEZÉSEK)
4. **Initialize this repository with**: NE pipáld a README-t (mi adjuk meg)
5. **Create repository**
6. **Add file → Upload files** → húzd be a teljes tartalmát ennek a `dotgithub-repo/` mappának (a 4 .md fájl + `profile/` almappa)
7. Commit message: "Initial org setup"
8. Commit directly to main

### Opció B: Git command line (gyorsabb ha terminálban érzed magad)

```bash
cd C:\Users\Barni\Projects\ForumHungaricum\dotgithub-repo

git init
git add .
git commit -m "Initial org setup"
git branch -M main
git remote add origin git@github.com:forum-hungaricum/.github.git
git push -u origin main
```

(Az utolsó parancs előtt a GitHub-on létre kell hozni az üres `.github` repot — Opció A 1-5. pontja.)

---

## Ellenőrzés

Telepítés után:

1. **Profile**: `https://github.com/forum-hungaricum` mutassa a `profile/README.md` tartalmát
2. **Security**: bármely repo-n a "Security" tab-on vagy a Repo-Insights-en jelenjen meg a SECURITY.md-re hivatkozás
3. **Code of Conduct**: bármely repo-n az **About** szakaszában jelenjen meg
4. **Contributing**: amikor valaki Issue-t vagy PR-t nyit, ajánlja fel a CONTRIBUTING.md-t

---

## Org-szintű beállítások (külön, GitHub Settings-en)

Ezek **nem a `.github` repo-n keresztül**, hanem **a GitHub org settings-en** állítandók be:

1. **Organization profile** (`https://github.com/organizations/forum-hungaricum/settings/profile`)
   - Display name: **Forum Hungaricum**
   - Description: *"A magyar számvetés 1990 óta. · Hungary's public-accountability infrastructure since 1990."*
   - URL: `https://forumhungaricum.eu`
   - Email: `kontakt@forumhungaricum.eu`
   - Twitter username: (még üres, később)
   - Location: *Hungary / Europe*

2. **Authentication security** (`https://github.com/organizations/forum-hungaricum/settings/security`)
   - **Require two-factor authentication for everyone in your organization** ✓
   
3. **Member privileges** (`https://github.com/organizations/forum-hungaricum/settings/member_privileges`)
   - **Base permissions**: Read (későbbi Triage-jogot tag-szinten)
   - Repository creation: **Owners only** (kontrollált)
   - Repository forking: **Allowed**
   - Pages creation: **Public sites allowed**
   - Repository visibility change: **Owners only**

4. **Email notifications** (`https://github.com/organizations/forum-hungaricum/settings/notifications`)
   - Restrict email notifications to verified domains (csak @forumhungaricum.eu)

---

## Mi NINCS itt (és miért)

- **LICENSE.md** ROOT-ban: nem teszünk az org-szintű repo-ba egységes licencet, mert a Forum Hungaricum **különböző licenceket** használ különböző repo-kban (CC BY-SA, MIT, AGPL, proprietary). Minden repo-ban saját LICENSE-t teszünk.
- **FUNDING.yml**: Sponsors / Patreon még nincs publikus, ha lesz, hozzáadjuk
- **ISSUE_TEMPLATE/**: első valós repo-knál tesszük be (méret-arány alapon)
- **PULL_REQUEST_TEMPLATE.md**: szintén első valós repo-knál

---

*Készítette: Claude (Cowork session, 2026-05-02). Bármi finomításra szorul, jelezd.*
