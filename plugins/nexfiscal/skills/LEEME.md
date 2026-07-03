# Skills del plugin NexFiscal

Las 8 skills del producto en su versión **cascarón**:

**Grupo A:** dictaminador-cfdi · calculadora-nomina-mx (piloto) · regimen-fiscal-optimo · calculadora-actualizacion-recargos
**Grupo B:** redactor-actas-asambleas · contratos-mercantiles · gestor-laboral-mx · compliance-lfpdppp

Reglas de toda skill de esta carpeta (ver CLAUDE.md del repo):

- La skill es cascarón: conversación, criterio, formato de reporte con marca y fundamentos legales estables.
- **Prohibido** incluir datos fiscales que caducan (UMA, tablas, tasas, listas SAT) o cálculos que dependan de ellos: todo se obtiene del connector `nexfiscal` (ver `.mcp.json` del plugin).
- La skill instruye de forma tajante usar el connector y **nunca** valores de memoria ni tablas locales.
- Sin suscripción activa la skill no entrega números: advierte que la suscripción venció y que los valores pueden estar desactualizados.

**Disponibles: las 8 de 8.**

- `calculadora-nomina-mx/` — nómina, finiquito, costo del trabajador y consultas de valores (cálculo 100% en el backend)
- `calculadora-actualizacion-recargos/` — actualización Art. 17-A, recargos por mora (SAT/IMSS/INFONAVIT), parcialidades/diferido y saldos a favor, con INPC y tasas en vivo (cálculo 100% en el backend)
- `regimen-fiscal-optimo/` — comparativo de carga fiscal RESICO PF / AEP / arrendamiento / plataformas / PM, con tablas, topes y costos en vivo (cálculo 100% en el backend)
- `dictaminador-cfdi/` — validación de CFDI 4.0 con catálogos del Anexo 20, reglas de consistencia y **listas 69/69-B/69-B Bis verificadas en vivo** con fecha de corte (datos 100% del backend)
- `gestor-laboral-mx/`, `contratos-mercantiles/`, `redactor-actas-asambleas/`, `compliance-lfpdppp/` — generación de documentos sobre ley estable; los valores que caducan (UMA, multas en pesos) se consultan al connector
