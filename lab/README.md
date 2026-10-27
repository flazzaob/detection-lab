# Laboratorio

## Arquitectura

```
   Hyper-V                              Docker
 +-----------------+               +--------------------+
 |  VM Windows 11  |  Winlogbeat   |  Elasticsearch     |
 |  + Sysmon       | ------------> |  + Kibana          |
 |  (victima)      |     :9200     |  (SIEM del lab)    |
 +-----------------+               +--------------------+
        ^
        | emulacion adversaria (Atomic Red Team)
```

La VM es donde se ataca. **Nunca en el equipo anfitrion.**

## Requisito previo

Virtualizacion activada en la BIOS. En placas AMD la opcion se llama **SVM Mode**,
normalmente bajo *Advanced -> CPU Configuration*.

Comprobacion desde PowerShell:

```powershell
systeminfo | Select-String "Virtualizaci"
```

Debe decir que la virtualizacion **si** esta habilitada en el firmware. Si dice que
no, ni Docker ni Hyper-V ni WSL van a funcionar.

## Arranque del SIEM

```bash
cd lab
docker compose up -d
```

Kibana queda en http://localhost:5601 . Sin autenticacion: es un laboratorio
aislado y no se expone a la red.

## Pendiente

- [ ] Activar SVM en la BIOS
- [ ] `wsl --install` y arrancar Docker Desktop
- [ ] Levantar Elasticsearch y Kibana
- [ ] Crear la VM Windows en Hyper-V
- [ ] Instalar Sysmon con una configuracion de referencia
- [ ] Instalar Winlogbeat y comprobar que llegan eventos a Kibana
