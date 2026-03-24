# Enjambre: Diagnóstico de la Trilogía Fiscal EPT

**Fecha**: 23 de marzo de 2026
**Corpus analizado**: 3 textos (trilogía fiscal completa)
**Alcance**: Paper 1 (5635152) leído pp. 1-5; Paper 2 (5645070) leído pp. 1-5; Paper 3 (draft) leído completo.

---

## Estado de coherencia

### Tensiones identificadas

**T1. El CLI mide cosas distintas en cada paper sin explicitarlo.**

En el Paper 1, CLI_14bis = 0.89 se refiere al lock-in del impuesto a las ganancias y la reforma laboral. En el Paper 3, CLI_copart = 0.997 se refiere al lock-in de la coparticipación. La fórmula es la misma pero los parámetros son diferentes (A, Y, E). El problema: el Paper 3 dice "CLI_copart (0.997) > CLI_14bis (0.89)" como si fueran comparables. Pero la variable E (entrenchment) vale 0.99 para coparticipación y un valor diferente para 14bis. Si la diferencia viene sobre todo del parámetro E, la comparación es trivial (mecanismos de reforma más exigentes producen CLI más altos, por definición). Para que la comparación sea informativa, el Paper 3 debería descomponer qué parte de la diferencia viene de E (estructura constitucional) y qué parte de A/Y (fracaso empírico de intentos).

**Evaluación**: tensión real, resoluble con una tabla que descomponga los componentes del CLI en ambos casos.

**T2. El Paper 2 dice que la reforma es posible (35-58%); el Paper 3 dice que es casi imposible (11.2% sin shock, 36.3% con FMI+Milei).**

El Paper 2 propone un mecanismo de scaffolding externo con P(reforma) = 35-58% en 8-12 años. El Paper 3 calcula P(reforma) = 36.3% para FMI+Milei combinados. La convergencia numérica es accidental pero sugerente: ambos papers están de acuerdo en que la reforma tiene alrededor de 35% de probabilidad bajo las mejores condiciones actuales. La diferencia es de *framing*: el Paper 2 presenta 35% como esperanza; el Paper 3 presenta 36% como insuficiencia.

**Evaluación**: tensión productiva, no contradictoria. Recomendación: el Paper 3 debería citar explícitamente el mecanismo del Paper 2 y mostrar que el scaffolding externo es la única vía para acercarse al 50% sin crisis. Esto cierra la trilogía: diagnóstico (Paper 1) → costo (Paper 3) → prescripción (Paper 2).

**T3. El Paper 1 menciona 47 reform bills; el Paper 3 dice 9 reform attempts.**

El Paper 1 dice "47 comprehensive tax reform bills" desde 1994 con 0% success rate. El Paper 3 dice "9 documented reform attempts" para coparticipación desde 1996 con 0 successes. No son contradictorios (se refieren a objetos distintos: reforma tributaria integral vs. coparticipación específica), pero la discrepancia numérica (47 vs. 9) podría confundir al lector que lea ambos. El Paper 3 debería aclarar que los 9 intentos se refieren exclusivamente a la ley-convenio de coparticipación prevista por la DT6, no a la totalidad de intentos de reforma tributaria.

**Evaluación**: inconsistencia de alcance, resoluble con una nota al pie.

### Terminología divergente

| Concepto | Paper 1 | Paper 2 | Paper 3 | Recomendación |
|----------|---------|---------|---------|---------------|
| Lock-in constitucional | "Constitutional Mutation" + ESE | "Mount Improbable" + fitness peaks | CLI + VSI | Usar CLI como métrica transversal; "constitutional mutation" y "Mount Improbable" como metáforas complementarias |
| La reforma | "Fiscal Trilemma" (3 objetivos incompatibles) | "Cliff vs slope" (shock vs gradual) | "Punctuation threshold" (shock mínimo) | El trilemma del Paper 1 no aparece en el Paper 3; debería integrarse |
| Fracaso de reforma | "Negative feedback loop" | "Cliff-scaling probability P = 10^-11" | "Funnel of failure" | Compatibles, pero el "negative feedback" del Paper 1 (cada fracaso reduce la probabilidad futura) no está en el modelo del Paper 3 |
| Transferencias como problema | "Extended phenotype" | "Coordination cost" | "Exaptation" | "Extended phenotype" y "exaptation" son conceptos del mismo marco (Dawkins), pero no es lo mismo: el fenotipo extendido es la estructura; la exaptación es el cambio de función. El Paper 3 debería hacer esta distinción explícita |

### Redundancias

**R1. La genealogía Tiebout→Rodden se repite en los Papers 2 y 3.** Ambos papers presentan la misma cadena teórica (Tiebout, Oates, Kornai, Rodden). El Paper 3 la desarrolla más (agrega Salmon, Gervasoni), pero hay solapamiento sustancial. Recomendación: el Paper 3 debería citar al Paper 2 para la cadena básica y concentrarse en lo que agrega (Salmon, Gervasoni, Steinmo).

**R2. Los datos de India GST y Brasil EC 132 aparecen en ambos Papers 2 y 3.** El Paper 2 los desarrolla en profundidad; el Paper 3 los usa como benchmarks comparativos. La redundancia es aceptable si el Paper 3 cita al Paper 2 para el detalle y se limita a la tabla comparativa.

### Supuestos vulnerables

**S1. "Correlación = causalidad" en H1.** El Paper 3 reporta r = 0.96 entre FSPI y calidad democrática y construye una "cadena causal" de cuatro eslabones. Pero la correlación transversal (n=24, un solo momento) no puede establecer causalidad. El paper lo reconoce en limitaciones (Sección 7.4) pero la Sección 4.1 presenta los resultados como si la causalidad estuviera demostrada. Un revisor exigirá o bien análisis de panel (datos longitudinales) o bien variables instrumentales.

**S2. Los índices de calidad democrática no son los de Gervasoni.** El Paper 3 dice que usa "a composite measure drawing on Gervasoni's SDI framework" pero no es el SDI real. Esto es honesto pero arriesgado: un revisor podría decir que la correlación alta (r=0.96) se debe a circularidad (si el índice de calidad democrática fue construido *sabiendo* los valores de FSPI, la correlación es espuria). El paper debería explicitar cómo se construyó el índice y demostrar que es independiente del FSPI.

**S3. El modelo de punctuation probability es ad hoc.** La fórmula P(reform|s) = (p+s)/(p+s+CLI×V) no tiene derivación teórica; es una función logística elegida por conveniencia. Un revisor de *World Politics* o *AJPS* la objetaría. Recomendación: presentarla como "reduced-form heuristic" y no como modelo formal, o derivarla de un juego de negociación bilateral.

## Mapa de oportunidades

### Formalizaciones pendientes

**F1. El FSPI debería tener una versión dinámica.** El paper actual mide FSPI como un snapshot (un año). La versión dinámica (FSPI a lo largo del tiempo) permitiría testear la hipótesis de vestigialidad: ¿el FSPI de Formosa bajó con el tiempo? ¿El de CABA subió? Si la degradación es acumulativa, debería haber una tendencia temporal.

**F2. El modelo de exaptación debería formalizarse como un juego.** La exaptación F1→F2 está descrita verbalmente pero podría modelarse como un juego en el que el gobernador elige entre "invertir en desarrollo productivo" y "expandir empleo público". Si las transferencias son altas, la segunda estrategia domina. Esto conectaría la exaptación con la literatura de moral hazard y le daría un resultado de equilibrio derivable.

### Predicciones testeables

**P1. Si se eliminan las transferencias, ¿mejora la democracia subnacional?** Milei recortó TNA un 84% en 2024. Si el modelo es correcto, las provincias más afectadas deberían exhibir *mayor* competencia electoral en las próximas elecciones (2027). Esta es una predicción concreta y falsable.

**P2. Neuquén post-2023: ¿la alternancia mejora la calidad institucional?** La primera alternancia en 61 años ocurrió en 2023. Si el FSPI framework es correcto, deberían observarse mejoras en competencia electoral, pluralismo mediático y empleo privado en los próximos años.

### Flancos no cubiertos

**FC1. ¿Y si la correlación FSPI-democracia es espuria?** La objeción más fuerte es que tanto la baja calidad democrática como la alta dependencia fiscal son consecuencias de una tercera variable: el bajo desarrollo económico. Provincias pobres tienen poca base tributaria (bajo FSPI) *y* instituciones débiles (baja democracia) por las mismas razones históricas (legado colonial, aislamiento geográfico, baja urbanización). Gervasoni controla por PIB per cápita y la relación se mantiene; el Paper 3 debería replicar ese control explícitamente.

**FC2. La objeción del "bien necesario".** Un defensor del sistema actual diría: sin coparticipación, Formosa no puede pagar maestros ni médicos. La degradación democrática es un costo aceptable de la equidad territorial. El Paper 3 no aborda esta objeción directamente. Recomendación: incorporar una sección que reconozca el trade-off equidad-democracia y proponga que el scaffolding externo del Paper 2 resuelve ambos simultáneamente.

## ¿Forman una trilogía coherente?

Sí, con ajustes. La arquitectura lógica es clara:

| Paper | Pregunta | Respuesta |
|-------|----------|-----------|
| 1 (5635152) | ¿Por qué la reforma es imposible? | Porque el sistema es un ESE con lock-in multinivel |
| 3 (draft) | ¿Cuál es el costo de la imposibilidad? | Degradación democrática subnacional (FSPI → clientelismo → feudalismo) |
| 2 (5645070) | ¿Cómo salir del ESE? | Scaffolding externo con compensación gradual (Mount Improbable) |

El orden de lectura natural es 1→3→2 (diagnóstico→costo→prescripción), pero fueron publicados 1→2→3. El Paper 3 debería explicitar que completa la trilogía llenando el eslabón faltante: el Paper 1 demostró el lock-in; el Paper 2 propuso la salida; el Paper 3 demuestra *por qué la salida es urgente* al cuantificar el daño democrático acumulativo.

## Prioridades sugeridas

1. **Resolver S2 (índice de calidad democrática)**: es la vulnerabilidad más grave. Si un revisor demuestra circularidad, todo H1 se cae. Solución: usar un proxy exógeno (Gervasoni SDI publicado, o ITPP de CIPPEC) en lugar del índice construido ad hoc.

2. **Integrar el Fiscal Trilemma del Paper 1 en el Paper 3**: el trilemma (constitucionalidad + sostenibilidad + autonomía provincial) debería aparecer en la Sección 7 como marco para las policy implications.

3. **Explicitar la distinción entre extended phenotype y exaptation**: son conceptos del mismo programa teórico (Dawkins) pero con funciones analíticas diferentes. El Paper 1 usa "extended phenotype" para la estructura; el Paper 3 usa "exaptation" para el cambio de función. Hacer esto explícito fortalece ambos.

4. **Agregar la predicción Milei-2024 como test empírico**: el recorte del 84% en TNA es un cuasi-experimento natural. Si el modelo es correcto, las elecciones provinciales de 2027 deberían mostrar mayor competencia en las provincias más afectadas. Incluir esta predicción haría al paper falsable.
