# Análisis acústico de dos melodías en violín

Proyecto individual del curso CA-0204 Herramientas de Ciencia de Datos I, Universidad de Costa Rica, II ciclo 2026.

**Autora:** María José Angulo Salas

## Descripción

Se compara el rango, la distribución y la evolución temporal de la altura musical en dos fragmentos interpretados y grabados en violín:
**Recuérdame** y **When You Wish Upon a Star**. 

En cada grabación se estima la frecuencia fundamental cada 0.025 segundos por autocorrelación, se valida contra las partituras y se convierte a semitonos (escala MIDI) para comparar las dos melodías con tablas y gráficos.

## Estructura del proyecto
- `cod/`: Documento Quarto con el código y el informe.
- `data/`: Grabaciones originales en formato M4A
- `info/`: Documentación y registro de las pruebas del método
- `config/`: Parámetros del análisis
- `res/`: gráficos generados para la presentación e informe final en PDF. 

## Requisitos

- R 4.4 o superior y RStudio.
- Quarto, con salida a PDF mediante Typst (incluido en Quarto).
- Paquetes de R. Se instalan una sola vez desde la consola:

```r
install.packages(c("av", "tuneR", "seewave", "soundgen", "tidyverse", "tinytable", "ragg"))
```
## Cómo reproducir el análisis

1. Clonar o descargar este repositorio.
2. Abrir `Individual_Angulo_HerramientasDatosI_2026.Rproj` en RStudio.
3. Abrir `cod/Individual_Angulo_HerramientasDatosI_2026.qmd`.
4. Presionar **Render**. El documento convierte los audios a WAV, estima las frecuencias y genera el informe en PDF.
(La estimación de frecuencias tarda unos minutos).

## Herramientas

- **R** y **RStudio**: lenguaje y entorno de análisis.
- **Quarto**: informe reproducible.
- **Git y GitHub**: control de versiones.
- Paquetes: `av` (conversión de audio), `tuneR` (lectura de WAV), `seewave` (espectrograma), `soundgen` (estimación de la frecuencia fundamental), `tidyverse` (datos y gráficos) y `tinytable` (tablas).
