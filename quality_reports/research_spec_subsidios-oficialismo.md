# Research Specification: Subsidios provinciales y voto al oficialismo en la provincia de Buenos Aires

**Fecha:** 2026-10-16 · **Fuente:** `/discover interview` con el autor · **Requisitos detallados:** `quality_reports/specs/2026-10-16_subsidios-oficialismo.md`

## Research Question

¿Cuánto explica el gasto provincial en subsidios, y cuál de sus seis tipos, el voto al oficialismo de la provincia de Buenos Aires en las elecciones nacionales, provinciales y municipales de 2021, 2023 y 2025, y qué implica eso para 2027?

## Motivation

La pregunta de fondo es si los votantes premian la gestión. Importa para la política pública y para decidir cómo asignar el gasto antes de un año electoral: si cada tipo de subsidio rinde distinto en votos, eso afecta la focalización y el diseño de los programas. El caso es útil porque desde diciembre de 2023 el oficialismo provincial (Kicillof) y el nacional (Milei) son rivales, así que el crédito por un subsidio provincial no se confunde con el del gobierno nacional.

## Hypothesis

1. Las transferencias directas a hogares (Plan Más Vida, dispositivos de niñez y adolescencia) tienen el mayor efecto sobre el voto provincial.
2. Los subsidios a obra pública y a caminos rurales se notan sobre todo en la categoría municipal (intendente).
3. El subsidio energético tiene poco efecto, porque su focalización es pobre.
4. En los municipios con intendente opositor, la provincia canaliza los fondos a instituciones y cooperativas locales. Con eso mejora el resultado del candidato del oficialismo provincial a intendente (ejemplo: Lanús, JxC en 2019 y UxP en 2023).
5. El efecto total es moderado: el autor se sorprendería si fuera grande.

## Empirical Strategy

- **Diseño:** panel de los 135 partidos. Se estima el cambio en el voto al oficialismo provincial respecto de 2019 (cuando ese espacio todavía no gobernaba) en función del gasto en subsidios per cápita entre una elección y otra, con efectos fijos de elección por categoría:
  $\Delta V_{m,t}^{c} = \alpha_t^{c} + \sum_k \beta_k^{c} S_{k,m,t} + X_m'\gamma + \varepsilon_{m,t}$, con $k$ el tipo de subsidio y $c$ la categoría.
- **Tratamiento:** monto deflactado (IPC mensual de INDEC) y cantidad de expedientes por partido. La fecha de aprobación define el tratamiento en la especificación principal; la de pago se usa como robustez.
- **Supuesto de identificación:** sin el gasto, el cambio de voto respecto de 2019 no estaría relacionado con el gasto asignado, una vez condicionado en vulnerabilidad y en los controles.
- **Amenaza principal:** la asignación estratégica, es decir, gastar más donde se espera ganar o perder votos, y elegir el canal según el color del intendente.
- **Pruebas y robustez:**
  - placebo: el gasto posterior a 2019 no debería predecir el cambio de voto entre 2015 y 2019;
  - ventanas de 6 y 12 meses antes de cada elección;
  - fecha de pago en lugar de fecha de aprobación;
  - cantidad de expedientes en lugar de montos.
- **Candidato a evaluar en `/strategize`:** variación de la población elegible por el desfase entre el tope de 2 SMVM y la inflación, medida con los ingresos del Censo 2022 o de la EPH.
- **Proyección 2027:** los coeficientes estimados por el gasto de 2026–2027, por escenarios del efecto común de elección de 2027 (que no se puede estimar).

## Data

- **Subsidios:** registros del autor, uno por expediente, con municipio, tipo, receptor, fecha de aprobación, fecha de pago en una parte de los casos, y monto. Hay datos solo de beneficiarios, no de los no seleccionados.
- **Elecciones:** resultados por partido para 2015, 2017, 2019, 2021, 2023 y 2025, en las categorías nacional, provincial y municipal.
- **Controles:** partido político de cada intendente por periodo (lo tiene el autor), población y vulnerabilidad del Censo 2022, e IPC de INDEC.
- **Unidad:** partido × elección × categoría.

## Expected Results

El autor no tiene una magnitud a priori y espera un efecto moderado. Un efecto grande y estable en los tres tipos de categoría sería sospechoso de asignación estratégica. Un efecto concentrado en las transferencias directas confirmaría la hipótesis 1.

## Contribution

La contribución central es comparar seis tipos de subsidio dentro de un mismo gobierno y período. La literatura base estudia un solo programa (Manacorda, Miguel & Vigorito 2011) o transferencias federales agregadas (Levitt & Snyder 1997; Kriner & Reeves 2012; Brollo & Nannicini 2012). Hay dos contribuciones secundarias: la estrategia de rodear al intendente opositor, y la atribución de crédito con oficialismos provincial y nacional enfrentados.

## Open Questions

- Pocas observaciones para seis coeficientes (135 partidos × 3 elecciones): probablemente haga falta agrupar los subsidios o estimar con restricciones.
- Cómo tratar 2025, que tuvo dos elecciones: la provincial, desdoblada el 7 de septiembre, y la nacional de octubre.
- Definir la lista del oficialismo en cada categoría y elección cuando cambia el nombre de la coalición (FdT, UxP, Fuerza Patria).
- **Destino:** primero un informe de política pública para la gestión (en español) y luego un paper académico. Por ahora el manuscrito en `paper/` está en inglés.
