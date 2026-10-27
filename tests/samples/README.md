# Logs de muestra

Eventos de ejemplo para probar las reglas sin levantar el laboratorio entero.

Cada regla deberia tener al menos dos ficheros:

- `<regla>.positive.json` - evento que **debe** disparar la regla
- `<regla>.negative.json` - evento legitimo parecido que **no debe** dispararla

El negativo es el importante: sin el, una regla que alerta de todo pasa los tests.

**Nunca subir telemetria real** de un entorno de trabajo. Solo eventos generados en
el laboratorio, o anonimizados a mano.
