# Ciencia de Datos — 2.º Cuatrimestre

Repositorio correspondiente a la materia **Ciencia de Datos**. En este espacio se centralizan los trabajos prácticos, informes, datasets, notebooks y documentación desarrollados por el grupo durante la cursada.

## Integrantes del grupo

| Integrante | Legajo |
|---|---:|
| Abate, Matias Alessandro | 1152129 |
| Ares Garcia, Juan Manuel | 1176654 |
| Garberi, Tomas | 1116880 |
| Molina, Facundo Roman | 1115862 |
| Rubini, Lucas Franco | 1158539 |
| Sorondo, Juan | 1157196 |

## Proyectos

### Análisis exploratorio de elecciones presidenciales de EE. UU.

Trabajo práctico grupal orientado a estudiar la asociación entre indicadores socioeconómicos y demográficos a nivel estatal y los resultados de las elecciones presidenciales de Estados Unidos.

El proyecto contempla:

- Diseño de la investigación.
- Definición de la pregunta y el alcance del análisis.
- Selección y documentación de datasets.
- Registro de fuentes y trazabilidad de los datos.
- Análisis exploratorio y visualización.
- Documentación de las limitaciones del estudio.
- Declaración del uso de herramientas de inteligencia artificial.

Documentación disponible en [`informe-elecciones-eeuu/`](./informe-elecciones-eeuu/).

### Análisis de un dataset de autos usados

Trabajo práctico basado en un dataset de vehículos usados. El proyecto incluye la documentación del dataset y las indicaciones necesarias para trabajar con archivos de gran tamaño almacenados mediante Git LFS.

Documentación disponible en [`trabajo-dataset-autos-usados/`](./trabajo-dataset-autos-usados/).

## Estructura del repositorio

```text
ciencia-de-datos_2c/
├── informe-elecciones-eeuu/
│   ├── README.md
│   ├── 01-diseno-investigacion.md
│   ├── 02-diccionario-datos.md
│   ├── 03-fuentes-trazabilidad.md
│   └── 04-declaracion-uso-ia.md
├── trabajo-dataset-autos-usados/
│   ├── README.md
│   ├── cars.csv
│   └── .gitattributes
├── .gitattributes
└── README.md
```

La estructura puede ampliarse a medida que avancen los trabajos. Para los análisis reproducibles se recomienda organizar los archivos de la siguiente manera:

```text
data/
├── raw/          # Datos originales, sin modificaciones
└── processed/    # Datos limpios y transformados mediante código

notebooks/        # Notebooks de análisis exploratorio
src/              # Código fuente reutilizable
outputs/          # Gráficos, tablas y resultados finales
```

## Reproducibilidad

Para facilitar la revisión y reutilización de los trabajos:

1. Conservar los datos originales sin modificaciones.
2. Registrar las fuentes, URLs y fechas de consulta.
3. Generar los datos procesados mediante código o notebooks reproducibles.
4. Documentar los supuestos, decisiones metodológicas y limitaciones.
5. Indicar las versiones relevantes de las herramientas utilizadas.
6. No incluir credenciales, claves privadas ni información sensible en el repositorio.

## Git Large File Storage (Git LFS)

El proyecto de autos usados utiliza **Git LFS** para almacenar archivos CSV de gran tamaño. Antes de clonar o descargar ese trabajo, instalar y configurar Git LFS:

```bash
git lfs install
git clone https://github.com/matias-abate/ciencia-de-datos_2c.git
cd ciencia-de-datos_2c
git lfs pull
```

Si un archivo grande aparece como un archivo de texto pequeño con metadatos, ejecutar `git lfs pull` luego de instalar Git LFS.

## Tecnologías y herramientas

- Python y/o R para procesamiento y análisis.
- Jupyter Notebook para exploración interactiva.
- Pandas, NumPy y herramientas de visualización, según corresponda.
- Git y GitHub para control de versiones y colaboración.
- Git LFS para archivos de gran tamaño.

## Estado del repositorio

El repositorio se encuentra en desarrollo y se actualizará con nuevos análisis, notebooks, visualizaciones y conclusiones a medida que avance la cursada.

## Autores

Trabajo realizado por los integrantes del grupo de la materia **Ciencia de Datos — 2.º Cuatrimestre**.
