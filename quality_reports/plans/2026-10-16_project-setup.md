# Plan: estructura del proyecto "Subsidios y voto al oficialismo"

**Status:** DRAFT (aprobación vía PR en borrador)

## Approach
Adaptar la plantilla al proyecto sin correr el pipeline: rellenar `CLAUDE.md`, el perfil de dominio,
la bibliografía base y un esqueleto de `paper/main.tex` con secciones vacías en el orden de
`paper-organization.md` §5. Las decisiones de fondo (país, subsidio, diseño) quedan para
`/discover interview` y `/strategize`.

## Files
- `CLAUDE.md` — nombre, campo, estado del proyecto
- `.claude/references/domain-profile.md` — economía política
- `Bibliography_base.bib` — 9 referencias del autor
- `paper/main.tex`, `paper/sections/*.tex` — esqueleto
- `paper/preambles/header.tex` — `\addbibresource` apunta a `Bibliography_base.bib`
- `quality_reports/specs/2026-10-16_subsidios-oficialismo.md` — spec con puntos abiertos
- `master_supporting_docs/supporting_papers/README.md` — mapa PDF ↔ clave BibTeX

## Verify
`cd paper && latexmk main.tex`; `python3 scripts/check_scaffold.py`; `python3 scripts/paper_coherence.py`.

## Next
1. `/discover interview` 2. `/discover lit` 3. `/discover data` 4. `/strategize`
