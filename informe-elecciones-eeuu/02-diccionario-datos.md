# 2. Selección de datasets y variables

## 2.1 Criterios de selección
Un dataset fue seleccionado solamente si cumple los siguientes criterios:

1. **Autoridad:** es publicado por una institución pública oficial de Estados Unidos.
2. **Trazabilidad:** permite registrar una URL estable, fecha o identificador de publicación y fecha de consulta.
3. **Granularidad:** está disponible a nivel estatal, incluyendo el Distrito de Columbia cuando corresponda.
4. **Alineación temporal:** puede asociarse a una elección presidencial sin utilizar información posterior a la elección.
5. **Claridad de definición:** documenta numerador, denominador, cobertura geográfica y método de estimación.
6. **Reproducibilidad:** el archivo original puede conservarse y su procesamiento puede realizarse mediante código.

## 2.2 Datasets seleccionados

| Dataset | Institución | Rol | Geografía / período | Motivo de selección |
|---|---|---|---|---|
| Resultados de elecciones federales | Federal Election Commission (FEC) | Resultado electoral | Estados + DC; 2012, 2016, 2020 y 2024 | Compilaciones oficiales de resultados federales certificados e informados por oficinas electorales estatales. |
| American Community Survey (ACS), estimaciones de 5 años | U.S. Census Bureau | Contexto explicativo | Estados + DC; estimaciones finalizadas en 2011, 2015, 2019 y 2023 | Estimaciones oficiales, documentadas y comparables sobre condiciones sociales, económicas y demográficas. |
| Election Statistics, 1920-presente | Office of the Clerk, U.S. House of Representatives | Fuente histórica y de contraste | Elecciones federales, 1920-presente | Serie histórica oficial; se conserva como contexto y posible validación, pero no se integra como fuente primaria del resultado presidencial en la primera etapa. |

## 2.3 Variables

| Variable | Rol | Definición / cálculo | Tabla ACS candidata | Escala esperada |
|---|---|---|---|---|
| `dem_two_party_share` | Resultado | Votos demócratas / (votos demócratas + votos republicanos) × 100 | Archivo de resultados FEC | Porcentaje |
| `total_votes_two_party` | Control / contexto | Votos demócratas + votos republicanos | Archivo de resultados FEC | Conteo |
| `median_household_income` | Explicativa | Ingreso mediano de los hogares en dólares ajustados por inflación; documentar versión ACS y base monetaria | S1901 | USD |
| `bachelors_or_higher_pct` | Explicativa | Población de 25 años o más con licenciatura universitaria o nivel superior / población de 25 años o más × 100 | DP02 | Porcentaje |
| `unemployment_pct` | Explicativa | Fuerza laboral civil desocupada / fuerza laboral civil × 100; usar la definición ACS | DP03 | Porcentaje |
| `non_hispanic_white_pct` | Explicativa | Población blanca no hispana / población total × 100 | DP05 | Porcentaje |
| `age_65_plus_pct` | Explicativa | Población de 65 años o más / población total × 100 | DP05 | Porcentaje |
| `state_fips` | Clave de unión | Código estatal FIPS de dos dígitos | Ambas fuentes, luego de normalizar | Texto |
| `election_year` | Clave de unión | 2012, 2016, 2020 o 2024 | Derivada | Entero |

**Fundamentación de las variables:** están disponibles de manera consistente en las publicaciones ACS, son interpretables a nivel estatal y representan dimensiones amplias de composición socioeconómica y demográfica. Se limita la cantidad inicial de variables para evitar buscar muchas asociaciones hasta encontrar una correlación espuria.

## 2.4 Emparejamiento temporal

| Año electoral | Estimación ACS de 5 años utilizada | Motivo |
|---|---:|---|
| 2012 | 2007-2011 | Última estimación quinquenal completa finalizada antes de la elección. |
| 2016 | 2011-2015 | Última estimación quinquenal completa finalizada antes de la elección. |
| 2020 | 2015-2019 | Última estimación quinquenal completa finalizada antes de la elección. |
| 2024 | 2019-2023 | Última estimación quinquenal completa finalizada antes de la elección. |

Este diseño prioriza la precedencia temporal: la medición contextual ocurre antes del resultado electoral. El costo es que cada valor ACS resume varios años anteriores y no solamente el año de la elección.

## 2.5 Variables excluidas en la primera etapa
- **Gasto de campaña:** puede ser relevante, pero requiere definir con cuidado cómo agregar gastos de candidatos y comités.
- **Encuestas de opinión:** miden un concepto distinto y tienen sus propios tiempos de trabajo de campo y metodologías.
- **Respuestas de encuestas individuales:** permiten responder otras preguntas, pero requieren microdatos, ponderaciones y una interpretación cuidadosa de privacidad.

Estas dimensiones podrán evaluarse en una fase posterior, una vez validado el proceso central de datos.
