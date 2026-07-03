# Skills del plugin NexFiscal

Aquí vivirán las 8 skills en su versión **cascarón** (Fase 4 del plan):

**Grupo A:** dictaminador-cfdi · calculadora-nomina-mx (piloto) · regimen-fiscal-optimo · calculadora-actualizacion-recargos
**Grupo B:** redactor-actas-asambleas · contratos-mercantiles · gestor-laboral-mx · compliance-lfpdppp

Reglas de toda skill de esta carpeta (ver CLAUDE.md del repo):

- La skill es cascarón: conversación, criterio, formato de reporte con marca y fundamentos legales estables.
- **Prohibido** incluir datos fiscales que caducan (UMA, tablas, tasas, listas SAT) o cálculos que dependan de ellos: todo se obtiene del connector `nexfiscal` (ver `.mcp.json` del plugin).
- La skill instruye de forma tajante usar el connector y **nunca** valores de memoria ni tablas locales.
- Sin suscripción activa la skill no entrega números: advierte que la suscripción venció y que los valores pueden estar desactualizados.

**Ya disponible:** `calculadora-nomina-mx/` (nómina regular, finiquito, costo del trabajador y consultas de valores) — refactor a cascarón de la skill original, conectada al backend de producción `mcp.nexfiscal.app`. Las 7 restantes se suman con este mismo patrón (Grupo A primero).
