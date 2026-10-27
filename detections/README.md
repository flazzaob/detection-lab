# Reglas de deteccion

Formato [Sigma](https://github.com/SigmaHQ/sigma). Una regla por fichero, nombrado
`<tecnica-attack>-<descripcion-corta>.yml`.

## Criterio de aceptacion

Una regla no entra aqui hasta que cumple las cinco condiciones:

1. **Mapeada** a una tecnica concreta de MITRE ATT&CK.
2. **Fuente declarada**: que log exacto la alimenta y que configuracion hace falta
   para que ese log exista.
3. **Validada**: se ha emulado el ataque y se ha visto disparar. Una regla no
   ejecutada es una hipotesis, no una deteccion.
4. **Falsos positivos documentados**: que actividad legitima la va a activar. Si el
   campo esta vacio es que no se han pensado, no que no los tenga.
5. **Nivel justificado**: por que es `high` y no `medium`.

## Organizacion

- `windows/` - endpoint: procesos, credenciales, persistencia, evasion
- `identity/` - autenticacion, tokens, OAuth, correo
- `cloud/` - plano de control de los proveedores
