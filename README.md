# Ciencia de Datos - Autos Usados

Dataset de análisis de vehículos usados.

## Requisitos Previos

Este proyecto utiliza **Git Large File Storage (LFS)** para almacenar archivos CSV grandes. Asegúrate de tener Git LFS instalado antes de clonar el repositorio.

### Instalar Git LFS

**macOS (Homebrew):**
```bash
brew install git-lfs
git lfs install
```

**Linux (Debian/Ubuntu):**
```bash
sudo apt-get install git-lfs
git lfs install
```

**Windows:**
Descarga el instalador desde: https://git-lfs.com/

## Clonar el Repositorio

Una vez que tengas Git LFS instalado:

```bash
git lfs install
git clone https://github.com/matias-abate/ciencia-de-datos_CarsUsed.git
cd ciencia-de-datos_CarsUsed
```

## Archivos del Proyecto

- **cars.csv** - Dataset principal de vehículos usados (~145 MB) - Almacenado con Git LFS

## Nota Importante

Si clonaste el repositorio **sin tener Git LFS instalado**, los archivos CSV aparecerán como archivos de texto pequeños con metadatos. Para solucionar esto:

1. Instala Git LFS
2. Ejecuta: `git lfs pull`
3. Los archivos se descargarán correctamente

## Estructura del Proyecto

```
ciencia-de-datos_CarsUsed/
├── cars.csv          # Dataset principal
├── README.md         # Este archivo
└── .gitattributes    # Configuración de Git LFS
```
