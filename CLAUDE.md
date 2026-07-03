# nexfiscal-skills — Repo público (marketplace + plugin)

Este repositorio **es el marketplace que agregan los clientes** en claude.ai (Customize → Plugins → Personal plugins → Add marketplace → desde repositorio). Mira hacia afuera: todo lo que se versione aquí lo verá el cliente.

Nota: el `CLAUDE.md` de este repo es para el DESARROLLO del repo (no se carga como contexto del plugin instalado; las instrucciones al modelo viven en cada SKILL.md).

## Reglas generales (obligatorias)

- Nunca hacer rollback, commit, push ni borrar archivos sin autorización explícita de Ernesto.
- Nunca asumir estructura de datos, enums ni nombres de campos: el contrato del connector vive en el repo privado `nexfiscal-skills-api` (`docs/CONTRATO-API-v1.md`) y de ahí salen los nombres de herramientas y campos.
- Entregar archivos completos y funcionales, no fragmentos, salvo cambio puntual.

## Reglas específicas de este repo — línea roja

- **Prohibido versionar aquí**: datos fiscales que caducan (UMA, tablas ISR, tasas, INPC, listas SAT, multas), cálculos que dependan de ellos, secretos, tokens, URLs internas o cualquier referencia al contenido del repo privado.
- Las skills son **cascarón**: flujo de conversación, criterio, formato de reporte con marca NexFiscal, fundamentos legales estables, y la instrucción tajante de usar el connector `nexfiscal` y **nunca** valores de memoria ni tablas locales.
- Degradación: sin suscripción activa la skill no entrega números como válidos; advierte que la suscripción venció y que los valores pueden estar desactualizados (el connector responde `suscripcion_inactiva`).
- Idioma: español, `snake_case` en identificadores, igual que el contrato.

## Estructura

```
.claude-plugin/marketplace.json      # catálogo del marketplace (este repo)
plugins/nexfiscal/
├── .claude-plugin/plugin.json       # manifiesto del plugin
├── .mcp.json                        # connector remoto (URL placeholder hasta Fase 3)
└── skills/calculadora-nomina-mx/    # 1.ª skill-cascarón (las 7 restantes, por fases)
```

## Estado

Backend en producción (https://mcp.nexfiscal.app), prueba de experiencia real en claude.ai superada, y plugin v0.4.0 con 6 de 8 skills publicadas: `calculadora-nomina-mx`, `calculadora-actualizacion-recargos` (ambas 100% backend), `gestor-laboral-mx`, `contratos-mercantiles`, `redactor-actas-asambleas` y `compliance-lfpdppp`. Faltan: `regimen-fiscal-optimo` y `dictaminador-cfdi` (Grupo A, requieren backend).
