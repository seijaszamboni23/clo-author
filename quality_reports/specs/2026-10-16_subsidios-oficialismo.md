# Requirements Specification: Subsidios y voto al oficialismo

**Date:** 2026-10-16
**Status:** DRAFT

---

## Objective

Estimar el efecto causal del gasto público en subsidios sobre el voto a los oficialismos, con un diseño de identificación creíble y datos administrativos a nivel territorial.

---

## Requirements

### MUST Have (Non-Negotiable)

- [ ] Resultado principal: proporción de votos del oficialismo por unidad territorial y elección ($V_{mt}$)
- [ ] Tratamiento: gasto en subsidios per cápita medido antes de cada elección ($S_{mt}$)
- [ ] Una estrategia de identificación explícita frente a la asignación táctica del gasto (ver `domain-profile.md`)
- [ ] Definición operativa de "oficialismo" por nivel de gobierno, coaliciones incluidas
- [ ] Datos y código reproducibles desde `data/raw/` con `scripts/R/`

### SHOULD Have (Preferred)

- [ ] Heterogeneidad por alineamiento político del gobierno local y por competitividad de la elección
- [ ] Participación electoral como resultado secundario (movilización vs. persuasión)
- [ ] Distinción entre subsidios discrecionales y asignados por regla

### MAY Have (Optional, If Time)

- [ ] Datos de encuestas sobre apoyo al gobierno (Latinobarómetro, LAPOP)
- [ ] Modelo formal de focalización (votante pivote vs. votante núcleo)

---

## Clarity Status

| Aspect | Status | Notes |
|--------|--------|-------|
| Pregunta general | CLEAR | Efecto del gasto en subsidios sobre el voto al oficialismo |
| País y periodo | BLOCKED | Por definir en `/discover interview` |
| Tipo de subsidio (transferencias a hogares, energía/transporte, productivos) | BLOCKED | Determina datos y diseño |
| Nivel de elección (nacional, subnacional) y de unidad (municipio, provincia, mesa) | ASSUMED | Municipio y elección nacional por defecto |
| Diseño de identificación | ASSUMED | Se elige con `/strategize`; candidatos en `domain-profile.md` |
| Idioma del manuscrito | ASSUMED | Inglés, para revistas internacionales |
| Tipo de paper | ASSUMED | Reduced-form |

---

## Success Criteria

- Pregunta, país, subsidio y diseño cerrados (sin filas BLOCKED)
- Fuentes de datos identificadas con acceso confirmado (`/discover data`)
- Revisión de literatura con la bibliografía base ampliada (`/discover lit`)

---

## Approval

[ ] User approved: [Date]
