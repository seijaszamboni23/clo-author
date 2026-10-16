# Requirements Specification: Subsidios y voto al oficialismo

**Date:** 2026-10-16
**Status:** DRAFT

---

## Objective

Estimar el efecto causal del gasto público en subsidios sobre el voto a los oficialismos en la provincia de Buenos Aires (Argentina), 2019–2027, con un diseño de identificación creíble y datos administrativos por municipio (135 partidos).

---

## Requirements

### MUST Have (Non-Negotiable)

- [ ] Resultado principal: proporción de votos del oficialismo por unidad territorial y elección ($V_{mt}$)
- [ ] Tratamiento: gasto en subsidios per cápita medido antes de cada elección ($S_{mt}$), por tipo:
  1. Transferencias a hogares: Plan Más Vida
  2. Subvenciones a dispositivos de cuidado de niñez y adolescencia
  3. Subsidios a la energía
  4. Subsidios a obra pública municipal
  5. Subsidios productivos a cooperativas (IPAC)
  6. Subsidios a caminos rurales
- [ ] Elecciones: 2019, 2021, 2023, 2025 (provinciales desdobladas el 7 de septiembre de 2025 y nacionales en octubre) y 2027 cuando haya resultados
- [ ] Una estrategia de identificación explícita frente a la asignación táctica del gasto (ver `domain-profile.md`)
- [ ] Definición operativa de "oficialismo" por nivel de gobierno, coaliciones incluidas. En la provincia gobierna Juntos por el Cambio hasta diciembre de 2019 y luego Frente de Todos / Unión por la Patria / Fuerza Patria (Kicillof). En la Nación, Juntos por el Cambio hasta 2019, Frente de Todos 2019–2023 y La Libertad Avanza desde diciembre de 2023. Además, cada intendente tiene su propio oficialismo municipal
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
| País y periodo | CLEAR | Provincia de Buenos Aires, 2019–2027 (respuesta del autor, 2026-10-16) |
| Tipos de subsidio | CLEAR | Los seis listados arriba |
| Elección de 2027 | ASSUMED | Todavía no ocurrió; el análisis principal usa 2019–2025 y 2027 se agrega cuando haya resultados |
| Unidad de análisis | ASSUMED | Municipio (partido); circuito o mesa si el gasto se puede georreferenciar |
| Nivel del oficialismo | ASSUMED | Oficialismo provincial como resultado principal; nacional y municipal como resultados secundarios |
| Nivel de gobierno que paga cada subsidio | BLOCKED | Confirmar en `/discover data` qué subsidios son provinciales y cuáles nacionales o mixtos (sobre todo energía), porque eso define a qué oficialismo se le atribuye el crédito |
| Disponibilidad de datos por municipio y año | BLOCKED | Confirmar en `/discover data` (presupuesto provincial, datos abiertos de la provincia, pedidos de acceso a la información) |
| Diseño de identificación | ASSUMED | Se elige con `/strategize`; candidatos en `domain-profile.md` |
| Idioma del manuscrito | ASSUMED | Inglés, para revistas internacionales |
| Tipo de paper | ASSUMED | Reduced-form |

---

## Success Criteria

- Nivel de gobierno, datos y diseño cerrados (sin filas BLOCKED)
- Fuentes de datos identificadas con acceso confirmado (`/discover data`)
- Revisión de literatura con la bibliografía base ampliada (`/discover lit`)

---

## Approval

[ ] User approved: [Date]
