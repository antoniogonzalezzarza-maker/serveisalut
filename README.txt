════════════════════════════════════════════════════════════
  OPOSICIONS IB-SALUT · Grup Tècnic Funció Administrativa
  Instruccions per afegir nous temes i tests
════════════════════════════════════════════════════════════

ESTRUCTURA DE CARPETES
──────────────────────
web-oposicions/
├── index.html          ← Portada principal (no modificar l'estructura)
├── style.css           ← Estils compartits (no modificar)
├── README.txt          ← Aquest fitxer
├── temes/
│   ├── tema12.html     ← Tema disponible
│   ├── tema13.html     ← Tema disponible
│   └── tema14.html     ← (quan estigui llest)
└── tests/
    ├── test_12_13.html ← Test disponible
    └── test_14_15.html ← (quan estigui llest)


COM AFEGIR UN NOU TEMA (ex: Tema 14)
──────────────────────────────────────
1. Copia el fitxer  temes/tema13.html  i anomena'l  temes/tema14.html
2. Edita el contingut:
   - Canvia el títol <title> i .tema-badge
   - Canvia el text del .tema-header h1 i p
   - Substitueix tot el contingut dins <div class="content">
   - Actualitza els pills de navegació (#seccions)
   - Actualitza el bottom-nav (← Tema 13 / Tema 15 →)
3. Obre index.html i localitza la targeta del Tema 14:
   - Canvia class="tema-card locked" per class="tema-card available"
   - Canvia href="temes/tema14.html" (ja ha d'estar posat)
   - Canvia l'span de status: de "🔒 Pròximament" a "✓ Disponible"
   - Canvia class="tema-status soon" per class="tema-status ok"
4. Actualitza el menú desplegable de navegació a index.html:
   - Afegeix: <a href="temes/tema14.html" class="nav-dropdown-item">Tema 14 — ...</a>
   - Fes el mateix a temes/tema12.html, temes/tema13.html i tests/test_12_13.html
5. Puja la carpeta actualitzada a Netlify (drag & drop)


COM AFEGIR UN NOU TEST (ex: Test 14-15)
─────────────────────────────────────────
1. Copia el fitxer  tests/test_12_13.html  i anomena'l  tests/test_14_15.html
2. Edita el títol i les dades de les preguntes dins el const RAW={...}
   seguint exactament la mateixa estructura:
   {
     q: "Text de la pregunta",
     opts: ["Opció a","Opció b","Opció c","Opció d"],
     c: 0,          ← índex de la resposta correcta (0=a, 1=b, 2=c, 3=d)
     bal: true,     ← opcional, afegeix etiqueta ★ Illes Balears
     exp: "Explicació que apareix en corregir"
   }
3. Obre index.html i activa la targeta del test corresponent:
   - Canvia class="test-card locked" per class="test-card available"
   - Canvia href i contingut del test-title i test-meta
4. Puja la carpeta actualitzada a Netlify


FÓRMULA DE PUNTUACIÓ
──────────────────────
Correcta:  +30/N punts   (N = nombre total de preguntes)
Errònia:   -(30/N)/4 punts
En blanc:  no permès
Mínim:     15/30 per superar l'exercici


COM PUBLICAR A NETLIFY
───────────────────────
1. Ves a https://netlify.com i inicia sessió
2. Al dashboard, arrossega la CARPETA (no el zip) a "Drop your site here"
3. Per actualitzar: arrossega la carpeta de nou → Netlify detecta els canvis
4. Per canviar la URL: Site settings → Change site name


ESTAT DELS CONTINGUTS (actualitzat: abril 2026)
─────────────────────────────────────────────────
✓ Tema 11 — disponible
✓ Tema 12 — disponible
✓ Tema 13 — disponible
✓ Test Tema 11 — disponible
✓ Test Temes 12-13 — disponible
🔒 Resta de temes i tests — pròximament


════════════════════════════════════════════════════════════
