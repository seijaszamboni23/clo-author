# Requirements Specification: Subsidios y voto al oficialismo

**Date:** 2026-10-16
**Status:** DRAFT

---

## Objective

Estimar el efecto causal del gasto público en subsidios sobre el voto a los oficialismos en la provincia de Buenos Aires (Argentina), 2019–2027, con un diseño de identificación creíble y datos administrativos por municipio (135 partidos).

---

## Diseño propuesto por el autor (2026-10-16)

- **Línea de base 2019:** el voto que obtuvo en 2019 el espacio que hoy gobierna la provincia (Frente de Todos), cuando todavía no era gestión, mide su base partidaria por partido.
- **Etapa de gestión:** en las elecciones de 2021, 2023 y 2025 se estima cuánto explican los subsidios provinciales entregados en cada partido (cantidad y monto) el cambio del voto respecto de 2019, en las categorías nacional, provincial y municipal.
- **Proyección 2027:** con los coeficientes estimados y el gasto de 2026–2027 se proyectan los votos del oficialismo provincial en las tres categorías.

Esquema: $\Delta V_{m,t}^{c} = V_{m,t}^{c} - V_{m,2019}^{c} = \alpha_t^{c} + \beta^{c} S_{m,t} + X_{m}'\gamma + \varepsilon_{m,t}$,
con $c \in \{\text{nacional}, \text{provincial}, \text{municipal}\}$, $S_{m,t}$ el gasto per cápita acumulado desde la elección anterior y $\alpha_t^{c}$ efectos fijos de elección que absorben el shock común (por ejemplo, la irrupción de LLA).

---

## Requirements

### MUST Have (Non-Negotiable)

- [ ] Resultado principal: proporción de votos de la lista del oficialismo provincial (FdT / UxP / Fuerza Patria) por partido, elección y categoría (nacional, provincial, municipal), en diferencias respecto de 2019
- [ ] Proyección 2027 por categoría, con intervalos y escenarios para el shock común de 2027
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
- [ ] Prueba placebo: el gasto posterior a 2019 no debe predecir el cambio de voto 2015→2019 (o 2017→2019)

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
| Oficialismo | CLEAR | La lista del espacio que gobierna la provincia, medida en las tres categorías (nacional, provincial, municipal) |
| Nivel de gobierno que paga cada subsidio | CLEAR | Los seis son provinciales (autor) |
| Disponibilidad de datos por municipio y año | CLEAR | El autor tiene cantidad de subsidios y montos por municipio; falta cargarlos en `data/raw/` |
| Frecuencia del gasto | ASSUMED | Anual; si hay datos mensuales se usa el gasto de los 12 meses previos a cada elección |
| Diseño de identificación | ASSUMED | Panel en diferencias respecto de 2019 con intensidad continua del gasto (arriba); `/strategize` lo valida. Amenaza principal: el gasto se asigna a partidos donde se espera ganar o perder votos |
| Proyección 2027 | ASSUMED | Condicional a escenarios para el efecto común de elección de 2027, que no se puede estimar |
| Idioma del manuscrito | ASSUMED | Inglés, para revistas internacionales |
| Tipo de paper | ASSUMED | Reduced-form con ejercicio de proyección |

---

## Success Criteria

- Datos de subsidios y resultados electorales cargados en `data/raw/` y documentados
- Diseño validado por el strategist-critic (`/strategize`)
- Revisión de literatura con la bibliografía base ampliada (`/discover lit`)

---

## Approval

[ ] User approved: [Date]
