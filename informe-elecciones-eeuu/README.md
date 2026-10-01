# Análisis exploratorio de elecciones presidenciales de EE. UU.

## Propósito
Este repositorio documenta el diseño inicial de una investigación **exploratoria** sobre las asociaciones entre indicadores socioeconómicos y demográficos a nivel estatal y los resultados de las elecciones presidenciales de Estados Unidos.

> **Importante:** este proyecto estudia correlaciones, no relaciones causales. Una correlación muestra que dos variables se comportan de manera relacionada en los datos observados; no demuestra que una haya causado a la otra.

## Integrantes del grupo
| Integrante | Legajo | Responsabilidad |
|---|---|---|
| _Abate, Matias Alessandro_ | _1152129_ | _Alumno_ |
| _Ares Garcia, Juan Manuel _ | _1176654_ | _Alumno_ |
| _Garberi, Tomas_ | _1116880_ | _Alumno_ |
| _Molina, Facundo Roman_ | _1115862_ | _Alumno_ |
| _Rubini, Lucas Franco_ | _1158539_ | _Alumno_ |
| _Sorondo, Juan_ | _1157196_ | _Alumno_ |

## Pregunta de investigación
**¿Cómo se asocian determinados indicadores socioeconómicos y demográficos a nivel estatal con la proporción de voto bipartidista demócrata en las elecciones generales presidenciales de EE. UU. entre 2012 y 2024?**

La proporción de voto bipartidista se calcula como `(votos demócratas / (votos demócratas + votos republicanos)) × 100`. Esto permite comparar elecciones con distinta participación de terceros partidos. Es una variable descriptiva, no una variable destinada a predecir resultados.

## Alcance
- **Unidad de análisis:** estado-año electoral (los 50 estados más el Distrito de Columbia).
- **Años electorales:** 2012, 2016, 2020 y 2024.
- **Elección:** solamente elección general presidencial.
- **Observaciones esperadas:** hasta 204 (51 jurisdicciones × 4 elecciones), sujetas a la disponibilidad de datos.

## Estructura del repositorio
- `docs/01-diseno-investigacion.md` — fundamentación, estado del arte, metodología y limitaciones.
- `docs/02-diccionario-datos.md` — datasets, variables y criterios de selección.
- `docs/03-fuentes-trazabilidad.md` — fuentes oficiales y plantilla para registrar descargas.
- `docs/04-declaracion-uso-ia.md` — borrador de declaración; reemplazar las partes pendientes con el texto oficial de la materia.
- `data/raw/` — copias inalteradas de los archivos descargados; no deben editarse.
- `data/processed/` — archivos limpiados y combinados de manera reproducible.
- `notebooks/` — notebooks para análisis exploratorio.
- `src/` — código reutilizable de limpieza y análisis.

## Regla de reproducibilidad
Conservar los archivos originales descargados en `data/raw/`, registrar su URL y fecha de acceso en `docs/03-fuentes-trazabilidad.md`, y generar todos los archivos de `data/processed/` mediante código. Esto preserva la **trazabilidad**: la posibilidad de reconstruir el origen de cada resultado.

## Estado actual
Diseño de investigación preparado. Falta completar los integrantes, el registro de descargas y la declaración de uso de IA aprobada por la cátedra.
