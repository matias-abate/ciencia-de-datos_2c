# 3. Fuentes, trazabilidad y registro de descargas

## Fuentes primarias

1. **Federal Election Commission (FEC), Election results and voting information**  
   https://www.fec.gov/introduction-campaign-finance/election-results-and-voting-information/  
   La FEC indica que compila los resultados de elecciones federales pasadas informados oficialmente por las oficinas electorales de estados y territorios. Sus publicaciones bienales *Federal Elections* incluyen resultados presidenciales cuando corresponde.

2. **U.S. House of Representatives, Election Statistics, 1920 to Present**  
   https://history.house.gov/Institution/Election-Statistics/Election-Statistics/  
   La oficina del Clerk of the House recopila y publica, desde 1920, los recuentos oficiales de elecciones federales provenientes de estados y territorios. Este proyecto la utiliza como referencia histórica y fuente de contraste.

3. **U.S. Census Bureau, American Community Survey 5-Year Data**  
   https://www.census.gov/data/developers/data-sets/acs-5year.html  
   ACS es una encuesta continua que ofrece información social, económica, habitacional y demográfica. Sus estimaciones de cinco años están disponibles para todos los estados y el Distrito de Columbia.

## Jerarquía de fuentes
Los totales electorales se tomarán de compilaciones oficiales, no de agregadores periodísticos. Si aparece una diferencia, la certificación de la oficina electoral del estado de origen es la referencia de mayor autoridad; la diferencia se documentará y no se sobrescribirá sin registro.

## Registro de descargas
Se completa una fila por cada archivo descargado. El **checksum SHA-256** es una huella digital del archivo: permite comprobar que se usa exactamente el mismo archivo original (`certutil -hashfile archivo SHA256` en Windows, `sha256sum archivo` en Linux/macOS).

| Archivo (`data/raw/`) | Dataset / año | Publicador | URL directa | Fecha de consulta | Formato | SHA-256 | Observaciones |
|---|---|---|---|---|---|---|---|
| Pendiente | Federal Elections 2012 | FEC | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | Federal Elections 2016 | FEC | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | Federal Elections 2020 | FEC | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | Federal Elections 2024 | FEC | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | ACS 5 años 2007-2011 (S1901, DP02, DP03, DP05) | U.S. Census Bureau | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | ACS 5 años 2011-2015 (S1901, DP02, DP03, DP05) | U.S. Census Bureau | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | ACS 5 años 2015-2019 (S1901, DP02, DP03, DP05) | U.S. Census Bureau | Pendiente | Pendiente | Pendiente | Pendiente | |
| Pendiente | ACS 5 años 2019-2023 (S1901, DP02, DP03, DP05) | U.S. Census Bureau | Pendiente | Pendiente | Pendiente | Pendiente | |

## Criterio de cita para el informe final
Citar autor institucional, título, año o versión cuando esté disponible, URL y fecha de consulta. La fecha de consulta es la fecha real de descarga registrada en la tabla anterior.
