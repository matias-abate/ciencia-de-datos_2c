# Análisis exploratorio de elecciones presidenciales de EE. UU.

## Propósito
Este repositorio documenta el diseño inicial de una investigación **exploratoria** sobre las asociaciones entre indicadores socioeconómicos y demográficos a nivel estatal y los resultados de las elecciones presidenciales de Estados Unidos.

> **Importante:** este proyecto estudia correlaciones, no relaciones causales. Una correlación muestra que dos variables se comportan de manera relacionada en los datos observados; no demuestra que una haya causado a la otra.

## Integrantes del grupo
| Integrante | Legajo |
|---|---|
| Abate, Matias Alessandro | 1152129 |
| Ares Garcia, Juan Manuel | 1176654 |
| Garberi, Tomas | 1116880 |
| Molina, Facundo Roman | 1115862 |
| Rubini, Lucas Franco | 1158539 |
| Sorondo, Juan | 1157196 |

## Pregunta de investigación
**¿Cómo se asocian determinados indicadores socioeconómicos y demográficos a nivel estatal con la proporción de voto bipartidista demócrata en las elecciones generales presidenciales de EE. UU. entre 2012 y 2024?**

La proporción de voto bipartidista se calcula como `(votos demócratas / (votos demócratas + votos republicanos)) × 100`. Esto permite comparar elecciones con distinta participación de terceros partidos. Es una variable descriptiva, no una variable destinada a predecir resultados.

## Alcance
- **Unidad de análisis:** estado-año electoral (los 50 estados más el Distrito de Columbia).
- **Años electorales:** 2012, 2016, 2020 y 2024.
- **Elección:** solamente elección general presidencial.
- **Observaciones esperadas:** hasta 204 (51 jurisdicciones × 4 elecciones), sujetas a la disponibilidad de datos.

## Estructura del repositorio
- [`01-diseno-investigacion.md`](01-diseno-investigacion.md) — fundamentación, estado del arte, metodología y limitaciones.
- [`02-diccionario-datos.md`](02-diccionario-datos.md) — datasets, variables y criterios de selección.
- [`03-fuentes-trazabilidad.md`](03-fuentes-trazabilidad.md) — fuentes oficiales y registro de descargas.
- [`04-declaracion-uso-ia.md`](04-declaracion-uso-ia.md) — declaración de uso de IA.

Cuando empiece la etapa de análisis se agregarán:
- `data/raw/` — copias inalteradas de los archivos descargados; no deben editarse.
- `data/processed/` — archivos limpiados y combinados de manera reproducible.
- `notebooks/` — notebooks para análisis exploratorio.

## Regla de reproducibilidad
Conservar los archivos originales descargados en `data/raw/`, registrar su URL y fecha de acceso en `03-fuentes-trazabilidad.md`, y generar todos los archivos de `data/processed/` mediante código. Esto preserva la **trazabilidad**: la posibilidad de reconstruir el origen de cada resultado.

## Estado actual
Diseño de investigación, selección de datasets y variables, fuentes y declaración de uso de IA completos. Próximos pasos: descargar los datos (completando el registro de descargas), unir FEC y ACS y comenzar el análisis exploratorio.
