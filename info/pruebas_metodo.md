# Pruebas del método de estimación de la frecuencia fundamental

Grabación de prueba: Recuérdame, compases 1 a 10, en Re mayor.
Rango según la partitura: Fa#4 (370 Hz) a Si5 (988 Hz).

## 1. seewave::fund() (método cepstral)
- Mínimo estimado: 73.1 Hz. Máximo: 1263.2 Hz.
- Descartado: 73.1 Hz está por debajo de la nota más grave del violín (Sol3, 196 Hz) y la función no permite fijar un límite inferior.

## 2. seewave::autoc() (autocorrelación)
- Parámetros: wl = 2048, fmin = 180, fmax = 1400, threshold = 5.
- Mínimo estimado: 421.1 Hz. Máximo: 1000 Hz.
- Descartado: no detectó Fa#4 ni Sol4. Con esos parámetros la función solo busca desde unos 403 Hz, porque sus límites no se aplican directamente en Hz.

## 4. Comprobación con los parámetros finales

Con el método elegido y los límites finales (pitchFloor = 300, pitchCeiling = 1250),
se comprobó qué porcentaje de las ventanas con sonido cae en notas esperadas.
Se calcula en el bloque validacion-notas del informe.

- Recuérdame: está en Re mayor y todas sus notas son de esa escala, así que se comparó
  la nota de cada ventana, sin octava, con las siete notas de Re mayor
  (Re, Mi, Fa#, Sol, La, Si, Do#). Resultado: [__ %].
- When You Wish Upon a Star: tiene alteraciones del arreglo (Fa#4, Sol#4, Do#5, Fa#5),
  así que se comparó la nota de cada ventana, con su octava, con las 17 notas escritas
  en los compases 22 a 25 y 34 a 41 de la partitura. Resultado: 98.3 %.
- Las ventanas que no coinciden corresponden sobre todo a cambios de nota.

