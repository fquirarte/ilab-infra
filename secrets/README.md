# Secretos

Los secretos **nunca se commitean a git**.

Cada servicio que necesita secretos tiene un archivo `.env` dentro de su carpeta
`compose/<servicio>/`. Estos archivos están excluidos por el `.gitignore` raíz.

## Convención

```
compose/
└── <servicio>/
    ├── docker-compose.yml   ← se commitea
    ├── .env.example         ← se commitea (muestra las variables requeridas, sin valores reales)
    └── .env                 ← NO se commitea
```

Siempre incluir un `.env.example` con los nombres de todas las variables y una descripción,
para que cualquiera que configure el servicio sepa qué llenar.
