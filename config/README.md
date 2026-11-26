# config

Parámetros del análisis. Están definidos dentro de `cod/Individual_Angulo_HerramientasDatosI_2026.qmd`; aquí se documentan sus valores y el motivo de cada uno.

| Parámetro | Valor | Dónde se usa | Motivo |
|---|---|---|---|
| Duración convertida de *Recuérdame* | 28.3 s | `conversion-audio` | El último fragmento del archivo M4A produce un error al decodificar |
| Duración convertida de *When You Wish Upon a Star* | 33.5 s | `conversion-audio` | Mismo motivo |
| Método de estimación | autocorrelación | `estimacion-f0` | Fue el único de los tres probados que coincidió con las partituras (ver `info/pruebas_metodo.md`) |
| Frecuencia mínima de búsqueda | 300 Hz | `estimacion-f0` | Un poco por debajo de la nota más grave de las partituras (Mi4, 330 Hz) |
| Frecuencia máxima de búsqueda | 1250 Hz | `estimacion-f0` | Un poco por encima de la nota más aguda de las partituras (Re6, 1175 Hz) |
| Límites de las zonas del registro | notas 71 y 78 (Si4 y Fa#5) | `tbl-zonas` | Dividen el registro de Mi4 a Re6 en tres zonas de amplitud aproximadamente igual.|
