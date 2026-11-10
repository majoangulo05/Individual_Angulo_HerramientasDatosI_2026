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

## 3. soundgen::analyze() (autocorrelación)
- Parámetros: pitchMethods = "autocor", pitchFloor = 350, pitchCeiling = 1100, priorMean = NULL.
- Nota más grave estimada: Fa#4. Nota más aguda: Si5. Coinciden con la partitura.
- El 97 % de las ventanas con sonido cae en notas de Re mayor.
- Método elegido.