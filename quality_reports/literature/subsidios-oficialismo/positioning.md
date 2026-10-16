# Posicionamiento: subsidios provinciales y voto al oficialismo (PBA)

**Fecha:** 2026-10-16 · **Ronda:** 2 · **Base:** `annotated_bibliography.md`, `frontier_map.md`

---

## 1. Propuesta de contribución

> Este trabajo es el primero en estimar los rendimientos electorales comparados de varios tipos de gasto de un mismo gobierno subnacional, sobre el mismo electorado y en el mismo período. Usa los registros de expedientes de seis subsidios de la provincia de Buenos Aires (transferencias a hogares, dispositivos de niñez y adolescencia, energía, obra pública municipal, subsidios productivos a cooperativas y caminos rurales) y el voto al oficialismo provincial en las categorías nacional, provincial y municipal de 2021, 2023 y 2025, con 2019 como base.

**Contra quién se diferencia:**

- **Literatura de un solo programa:**
  - Manacorda et al. (2011), De La O (2013), Zucco (2013), Conover et al. (2020) y Labonne (2013) estudian un programa por vez.
  - Pizzi (2026, provisional) estudia un subsidio energético nacional en una sola elección.
  - El proyecto compara tipos dentro de un mismo gobierno, como piden Kramon y Posner (2013), y extiende a seis tipos la comparación de dos de Healy y Malhotra (2009).
- **Literatura de transferencias agregadas:**
  - Levitt y Snyder (1997), Kriner y Reeves (2012) y Jones, Meloni y Tommasi (2012) estudian el gasto total.
  - El proyecto lo desagrega por tipo y por canal de pago.
- **Literatura argentina:** se centra en la asignación (Giraudy 2007; Simison 2015; Clerici et al. 2024) o en los mecanismos clientelares (Stokes et al. 2013; Zarazaga 2025). El proyecto estima rendimientos con la provincia como otorgante, que es un nivel casi sin estudiar. El único antecedente directo es Charpentier (2015), una tesis de grado sobre la asignación.

**Contribuciones secundarias:**

1. **Bypass:** la provincia canaliza fondos a instituciones y cooperativas en los municipios con intendente opositor.
   - Bueno (2018) documenta la asignación en Brasil, y Bonvecchi y Lodola (2011) documentan el bypass nación→provincia en Argentina.
   - El proyecto agrega el paso que falta: si el bypass mejora el voto del candidato del gobernador a intendente.
   - El contraste teórico lo dan Bracco et al. (2015) y Solé‑Ollé y Sorribas‑Navarro (2008 WP): si la obra pasa por el intendente, el crédito es del intendente.
2. **Atribución con oficialismos enfrentados:** desde diciembre de 2023 la provincia y la nación están gobernadas por rivales.
   - La predicción de Gasper y Reeves (2011) y Niedzwiecki (2016) es que los subsidios de atribución clara rinden al nivel que los paga, y que los recortes del otro nivel pueden beneficiar al gobernador.
   - Gélineau y Remmer (2006) advierten que en Argentina el voto subnacional es en buena parte un referéndum nacional, lo que debería achicar los efectos de los subsidios frente al efecto común de cada elección.

## 2. Revistas sugeridas

| Destino | Por qué |
|---|---|
| Journal of Politics, Comparative Political Studies | Donde se publicaron Bueno (2018), Niedzwiecki (2016) e Imai et al. (2020); atribución y política distributiva comparada |
| European Journal of Political Economy, Economics & Politics | Donde se publicaron Vergne (2009), Jones et al. (2012) y Porto y Sanguinetti (2001); economía política fiscal |
| Electoral Studies, Public Choice | Revistas de especialidad con la pregunta gasto→voto |
| LARR, LAPS, Desarrollo Económico | Público latinoamericanista; Corrêa (2015), Zarazaga (2014), Nazareno et al. (2006) |

Para el **informe de política** (primer producto, en español), los antecedentes más traducibles a recomendaciones son tres:

- Healy y Malhotra (2009), sobre qué tipo de gasto se premia;
- Bechtel y Hainmueller (2011) y Chen (2013), sobre cuánto dura el premio y cuándo debe llegar el gasto;
- Drazen y Eslava (2010), sobre la composición preelectoral.

## 3. Críticas previsibles y cómo prepararse

| # | Crítica | Fuente | Preparación sugerida (a evaluar en `/strategize`; el librarian no propone la identificación) |
|---|---|---|---|
| 1 | "Los programas reglados no rinden votos; los efectos positivos son artefactos" | Imai, King y Velasco Rivera (2020); Corrêa (2015) | Clasificar los seis tipos por discrecionalidad; reportar los nulos con la misma prominencia |
| 2 | "El gasto se asigna donde se esperan votos" | Giraudy (2007); Nazareno et al. (2006); Simison (2015); Dixit y Londregan (1996); Drazen y Eslava (2010) | El placebo 2015–2019 ya previsto; documentar el ciclo de composición; controlar el margen de 2019 |
| 3 | "Comparar seis $\beta_k$ en una regresión está contaminado" | Goldsmith‑Pinkham, Hull y Kolesár (2024) | Estimadores libres de contaminación o comparación tipo por tipo |
| 4 | "Comparar dosis no se identifica con la tendencia paralela estándar" | Callaway, Goodman‑Bacon y Sant'Anna (2024); de Chaisemartin et al. (2025) | Declarar el supuesto fuerte o reportar efectos por nivel de dosis |
| 5 | "Con 135 unidades la inferencia es frágil y los vecinos están correlacionados" | Cameron, Gelbach y Miller (2008); MacKinnon y Webb (2017); Conley (1999) | Wild cluster bootstrap; errores de Conley como robustez |
| 6 | "¿Quién se lleva el crédito?" | Cruz y Schneider (2017); Pop‑Eleches y Pop‑Eleches (2012); Labonne (2013) | Separar los resultados por categoría y por canal de pago; mirar el gasto municipal propio |
| 7 | "Es la nación, no la provincia" | Gélineau y Remmer (2006); Gasper y Reeves (2011); Clerici et al. (2024); Pizzi (2026) | Controlar los fondos nacionales a municipios (ATN), la Zona Fría y los recortes nacionales después de 2023 |
| 8 | "Es movilización, no persuasión" | De La O (2013); Chen (2013); Szwarcberg (2015) | Estimar también sobre la participación |
| 9 | "El efecto se evapora: la proyección a 2027 lo exagera" | Bechtel y Hainmueller (2011); Corrêa (2015); Linzer (2013) | Proyectar con decaimiento y con escenarios para $\alpha_{2027}$ |

## 4. Vacíos que llena el proyecto

1. Rendimientos electorales comparados de varios tipos de gasto de un mismo gobierno subnacional: no hay antecedente.
2. La provincia como otorgante en Argentina: no se encontraron estudios de efectos electorales.
3. Programas provinciales específicos (Más Vida, IPAC, caminos rurales, dispositivos de niñez): no hay estudios.
4. El rédito electoral del bypass por cooperativas e instituciones locales: Bueno (2018) documenta la asignación, no el voto.
5. La atribución con gobernador y presidente enfrentados en Argentina (2023–2025): no hay estudios académicos.

## 5. Riesgo de scooping

- **Pizzi (2026), provisional:** solapa en el subsidio energético y en la elección de 2021. Hay que conseguir el paper y citarlo como complemento: un subsidio nacional, de un solo tipo.
- **Arcidiacono (2023), sin verificar:** tesis MRes en Nottingham sobre viajes de egresados subsidiados. Si trata el programa bonaerense de 2021, es el antecedente más cercano en contexto. Hay que leerlo antes de redactar la contribución.
- No se encontraron working papers con la misma pregunta y los mismos datos en NBER, SSRN, IZA, CEDLAS, UdeSA, UTDT ni CIPPEC.
