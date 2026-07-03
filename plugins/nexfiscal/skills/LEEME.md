# Skills del plugin NexFiscal

Aquí vivirán las 8 skills en su versión **cascarón** (Fase 4 del plan):

**Grupo A:** dictaminador-cfdi · calculadora-nomina-mx (piloto) · regimen-fiscal-optimo · calculadora-actualizacion-recargos
**Grupo B:** redactor-actas-asambleas · contratos-mercantiles · gestor-laboral-mx · compliance-lfpdppp

Reglas de toda skill de esta carpeta (ver CLAUDE.md del repo):

- La skill es cascarón: conversación, criterio, formato de reporte con marca y fundamentos legales estables.
- **Prohibido** incluir datos fiscales que caducan (UMA, tablas, tasas, listas SAT) o cálculos que dependan de ellos: todo se obtiene del connector `nexfiscal` (ver `.mcp.json` del plugin).
- La skill instruye de forma tajante usar el connector y **nunca** valores de memoria ni tablas locales.
- Sin suscripción activa la skill no entrega números: advierte que la suscripción venció y que los valores pueden estar desactualizados.

**Disponibles (6 de 8):**

- `calculadora-nomina-mx/` — nómina, finiquito, costo del trabajador y consultas de valores (cálculo 100% en el backend)
- `calculadora-actualizacion-recargos/` — actualización Art. 17-A, recargos por mora (SAT/IMSS/INFONAVIT), parcialidades/diferido y saldos a favor, con INPC y tasas en vivo (cálculo 100% en el backend)
- `gestor-laboral-mx/`, `contratos-mercantiles/`, `redactor-actas-asambleas/`, `compliance-lfpdppp/` — generación de documentos sobre ley estable; los valores que caducan (UMA, multas en pesos) se consultan al connector

**En camino (Grupo A, requieren backend):** `regimen-fiscal-optimo` y `dictaminador-cfdi` (listas 69/69-B en vivo).
