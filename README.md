# Detection Lab

Laboratorio personal de ingenieria de deteccion: reglas propias, validadas contra
ataques emulados en un entorno controlado, y las notas tecnicas que las sustentan.

Cada deteccion de este repositorio esta escrita a mano, ejecutada contra telemetria
real generada en el laboratorio y documentada con sus falsos positivos conocidos.
**Nada se da por bueno sin haber visto la regla disparar.**

## Estructura

| Carpeta | Contenido |
|---|---|
| `detections/` | Reglas en formato Sigma, organizadas por dominio |
| `fichas/` | Notas tecnicas: que hace una tecnica, que la delata, que ruido genera |
| `tests/` | Logs de muestra y pruebas automaticas de las reglas |
| `lab/` | Infraestructura del laboratorio como codigo |
| `scripts/` | Utilidades en Python para el pipeline |

## Estado

En construccion. Fase actual: fundamento y telemetria de endpoint en Windows.

## Laboratorio

Ver [`lab/README.md`](lab/README.md) para la arquitectura y el arranque.
