# ilab-infra

Infraestructura-como-código del iLab, CUCEI — Universidad de Guadalajara.

## Propósito

El iLab es el laboratorio de innovación del CUCEI. Este repositorio formaliza la infraestructura
del laboratorio: documenta el servidor, estandariza el despliegue de aplicaciones y establece
una base sólida para que cualquier colaborador pueda entender, reproducir y extender el entorno
sin depender del conocimiento de una sola persona.

Un servidor. Docker Compose por servicio. Todo declarado en este repositorio.

## Stack

| Capa | Herramienta |
|---|---|
| SO | Ubuntu Server 24.04 LTS |
| Contenedores | Docker + Compose |
| Reverse proxy | Traefik |
| Visibilidad | Portainer |
| Modelos LLM | Ollama |
| Interfaz IA | Open WebUI |
| Agente IA | OpenClaw |
| Automatización | n8n |

## Servidor

| Campo | Valor |
|---|---|
| Ubicación | iLab, CUCEI — Universidad de Guadalajara |
| IP Pública | `148.202.11.15` |
| DNS | `ilab.cucei.udg.mx`, `*.ilab.cucei.udg.mx` |

## Estructura

```
ilab-infra/
├── docs/        Arquitectura y runbooks
├── inventory/   Inventario del servidor
├── compose/     Un directorio por servicio
├── configs/     Configuraciones compartidas
├── scripts/     Aprovisionamiento del SO
└── secrets/     Convención de manejo de secretos
```

## Convenciones

- Cada servicio vive en `compose/<nombre>/` con su `docker-compose.yml` y `README.md`
- Los secretos van en archivos `.env` locales, nunca en git
- Las versiones de imágenes siempre están fijadas

---

**iLab · CUCEI · Universidad de Guadalajara · 2026**
