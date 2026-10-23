# Proiectul „Disfagie”

Site-ul „Centru de Logopedie & Disfagie” — publicat pe Netlify:
https://spectacular-chimera-d11458.netlify.app

- Repository GitHub: `floreadanaandrei/logopedie-disfagie` (ramura `main`)
- Copie locală pe Mac-ul utilizatoarei: `/Users/floreadana/Claude/Projects/Website/Disfagie`
- Când utilizatoarea spune „proiectul Disfagie”, se referă la acest repository.
  (NU la `~/fotescu-website`, care e un alt site, mai vechi.)

## Regulă de lucru — obligatorie pentru orice modificare

Pentru fiecare modificare cerută:

1. Fă schimbarea în cod și verifică vizual pagina (ex. Playwright pe un server local).
2. Fă commit și **push pe GitHub** (`main`), ca Netlify să publice site-ul.
3. **Actualizează și copia locală** din `/Users/floreadana/Claude/Projects/Website/Disfagie`,
   ca utilizatoarea să aibă mereu ultima versiune pe calculator.

Nu considera sarcina încheiată până nu sunt făcuți toți cei trei pași.

### Note tehnice pentru pașii 2–3

- Commit-urile se fac cu `user.name=Claude`, `user.email=noreply@anthropic.com`.
- Shell-ul de pe Mac (device_bash) **nu poate accesa GitHub** (proxy 403). Pentru a
  sincroniza copia locală: creează un `git bundle` în cloud, copiază-l pe Mac
  (device_commit_files) și fă `git fetch <bundle> main:refs/remotes/origin/main`
  urmat de `git merge --ff-only origin/main` în folderul local.
- În folderele conectate de pe Mac ștergerea e blocată implicit, deci git poate lăsa
  fișiere `.lock` în `.git` — mută-le (ex. `.git/stale-...`), nu le lăsa pe loc.

## Structura site-ului

- `index.html` — pagina principală (HTML/CSS/JS static, fără build).
- `data/team.json` — specialiștii; pozițiile 1–3 corespund cardurilor
  `mihaela`, `specialist2`, `specialist3` din `index.html` (populate prin JS).
- `data/site.json` — texte pentru secțiuni (hero, despre disfagie, echipă, servicii, contact).
- `data/posts.json`, `posts/`, `blog.html` — blogul.
- `admin/` — Decap/Netlify CMS (`config.yml`), backend git-gateway.
- `images/` — fotografii.

## Stare actuală (de reținut)

- Poziția 2: Simona Cobârzan (Cluj-Napoca). Afilierile ei sunt „În curs de actualizare”
  până primește acordul asociațiilor (SRF, ASTTLR, APPA).
- Poziția 3: încă o intrare de test („Fotescu Andreu”, „Test 2”).
