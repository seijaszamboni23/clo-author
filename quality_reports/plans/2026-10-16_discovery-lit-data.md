# Plan: discovery (literatura y datos) — subsidios y voto al oficialismo en PBA

**Status:** DRAFT — pendiente de aprobación del autor

## Approach
1. `/discover lit`: librarian + librarian-critic. Parte de las 9 referencias de `Bibliography_base.bib` y amplía con
   transferencias y voto en Argentina (planes sociales, AUH, subsidios energéticos, federalismo fiscal y
   alineamiento intendente–gobernador) y la literatura internacional reciente.
2. `/discover data`: explorer + explorer-critic. Para cada uno de los seis subsidios, identifica fuente, nivel de
   gobierno que paga, desagregación (partido, año, mes), acceso (abierto o pedido de acceso a la información) y
   cobertura 2019–2025. También resultados electorales por partido/circuito y covariables del Censo 2022.

## Outputs
- `quality_reports/` bibliografía anotada + nuevas entradas en `Bibliography_base.bib`
- Evaluación de datos con un grado de factibilidad por subsidio
- Spec actualizado (filas BLOCKED resueltas o con próximo paso concreto)

## Verify
Críticos >= 80 (registrados en `quality_reports/research_journal.md`); `python3 scripts/score.py`.
