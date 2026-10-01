# 1. Diseño y fundamentación de la investigación

## 1.1 Fundamentación
Las elecciones presidenciales de Estados Unidos se resuelven a partir de resultados estatales en el Colegio Electoral, mientras que las condiciones sociales y económicas de la población difieren de manera considerable entre estados. Este proyecto analizará si determinadas características estatales medibles se asocian estadísticamente con la proporción de voto bipartidista demócrata en elecciones generales presidenciales.

El objetivo es construir un dataset inicial, transparente y reproducible, e identificar patrones que puedan investigarse con mayor profundidad. No se busca explicar el comportamiento electoral individual ni afirmar que una característica demográfica o económica cause un resultado electoral.

## 1.2 Tipo de estudio
El estudio es **cuantitativo, observacional y exploratorio**, con observaciones repetidas a nivel estatal.

- **Cuantitativo:** utiliza recuentos numéricos de votos y estimaciones numéricas de características poblacionales.
- **Observacional:** el equipo no manipula ninguna variable; analiza datos que ya fueron producidos por organismos públicos.
- **Exploratorio:** primero se describen distribuciones, se visualizan relaciones y se estiman asociaciones simples. No se pretende confirmar hipótesis causales.
- **Ecológico:** los datos representan estados, no votantes individuales. Por eso, no se pueden convertir patrones estatales en conclusiones sobre cada persona. Este error se denomina **falacia ecológica**.

## 1.3 Pregunta de investigación y operacionalización
**Pregunta:** ¿Cómo se asocian determinados indicadores socioeconómicos y demográficos con la proporción de voto bipartidista demócrata a nivel estatal en las elecciones presidenciales de 2012, 2016, 2020 y 2024?

**Variable de resultado:** proporción de voto bipartidista demócrata.

**Variables explicativas candidatas:** ingreso mediano de los hogares, proporción de población con título universitario, tasa de desempleo, proporción de población blanca no hispana y proporción de población de 65 años o más. Sus definiciones exactas y tablas de origen se detallan en `02-diccionario-datos.md`.

## 1.4 Estado del arte
La literatura sobre comportamiento electoral suele considerar la composición socioeconómica, el nivel educativo, la edad y la composición racial o étnica como factores contextuales relevantes. Este proyecto aporta un ejercicio descriptivo y reproducible que combina resultados electorales oficiales con estimaciones oficiales del Census Bureau en una misma escala geográfica: el estado.

Las variables seleccionadas no deben interpretarse como una explicación completa del voto. La competencia partidaria, las características de los candidatos, las campañas, las reglas electorales, la historia política de cada estado y las decisiones de medición también pueden influir. La existencia de estos factores no incluidos es una razón central para no usar lenguaje causal.

## 1.5 Plan de análisis
1. Descargar y conservar los resultados oficiales de elecciones generales presidenciales publicados por la FEC.
2. Extraer los votos estatales demócratas y republicanos, estandarizar los identificadores de estado y calcular la proporción de voto bipartidista.
3. Obtener estimaciones ACS de cinco años que terminen el año anterior a cada elección: 2011, 2015, 2019 y 2023. Esta decisión reduce el riesgo de utilizar información medida después de la elección.
4. Unir ambos datasets mediante el código FIPS estatal y el año electoral.
5. Revisar valores faltantes, filas duplicadas, rangos plausibles y denominadores de los porcentajes.
6. Generar estadísticas descriptivas, gráficos de dispersión, coeficientes de correlación de Pearson y Spearman, y regresiones lineales simples con intervalos de confianza.
7. Informar tamaños de efecto, incertidumbre y limitaciones; nunca presentar correlación como causalidad.

La **correlación de Pearson** mide una asociación lineal. La **correlación de Spearman** compara rangos y es menos sensible a valores extremos o a relaciones no lineales pero monotónicas. Usar ambas es una verificación de robustez, no una demostración.

## 1.6 Alternativas consideradas y decisión
- **Alternativa 1: análisis por condado.** Ofrece más observaciones, pero exige reconciliar límites administrativos, jurisdicciones especiales y posiblemente múltiples fuentes electorales. No se eligió para la primera etapa porque agrega complejidad de integración que puede ocultar la metodología básica.
- **Alternativa 2: serie temporal nacional.** Es más simple, pero solo tendría cuatro observaciones presidenciales en el período elegido; no es suficiente para un análisis de correlación con sustento.
- **Decisión: panel estado-año electoral.** Tiene una unidad de análisis manejable y auditable, se vincula con el contexto del Colegio Electoral y puede alcanzar 204 observaciones.

**Trade-off:** agregar los datos por estado simplifica la reproducción y la comunicación, pero pierde diferencias dentro de cada estado y no permite obtener conclusiones a nivel individual. Es parecido a calcular la temperatura promedio de toda una provincia: sirve para comparar provincias, pero no describe cada barrio.

## 1.7 Amenazas a la validez y limitaciones
- Los valores ACS son estimaciones de encuestas, no un censo de todas las personas; poseen márgenes de error.
- La estimación ACS de cinco años resume un período y no representa una medición puntual.
- La agregación estatal puede ocultar diferencias relevantes entre condados o personas.
- Las observaciones de un mismo estado en distintos años no son completamente independientes.
- La cantidad reducida de elecciones limita la inferencia temporal.
- Las definiciones de resultados electorales y las etiquetas de candidatos deben verificarse para cada año en la fuente oficial.
- Las correlaciones pueden verse afectadas por variables omitidas y valores extremos.

## 1.8 Uso ético de los datos
El análisis utiliza datos públicos agregados. Aun así, los resultados no deben estigmatizar grupos ni sugerir que una característica demográfica determina el voto de una persona. Los hallazgos se presentarán como asociaciones agregadas observadas.
