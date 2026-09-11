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

**Producto completo: 8 de 8 skills publicadas (plugin v0.6.0)** sobre el backend en producción (https://mcp.nexfiscal.app) con 8 herramientas del contrato v1.3. Grupo A 100% backend: nómina, recargos, régimen fiscal y dictaminador CFDI (listas 69/69-B en vivo). Grupo B: gestor laboral, contratos, actas y compliance LFPDPPP (actualizada a la LFPDPPP 2025 en el plugin v0.7.0, commit c23911a, con visto bueno de Ernesto).

**Plugin 0.9.4 (11-sep-2026):** limpieza de la numeración de la ley abrogada de 2010 en compliance-lfpdppp y contratos-mercantiles, contra una concordancia 2010→2025 verificada en el texto vigente de Diputados y en el DOF del 20-03-2025 (no contra la propia skill): aviso Art. 17→16 y 'a partir de que se recaban', gratuidad ARCO 35→34, transferencias 37→36 y 36→35, causas de negativa Art. 33, plazos ARCO Art. 31; 'persona o departamento de datos personales' (Art. 29) en lugar de 'encargado', que en la ley es otra figura; la autoridad sancionadora ya no es el INAI sino la Secretaría Anticorrupción y Buen Gobierno; y se corrigió que la ley abrogada tenía 11 fracciones en el aviso (tenía 6). **Quedó apartado para visto bueno de Ernesto** lo que cambia la asesoría y no solo la cita: la cláusula de aceptación de transferencias como obligatoria (Art. 35), el contenido mínimo del aviso simplificado y la advertencia sobre el aviso corto (Art. 16 fracc. II), los mecanismos de revocación (Art. 7) si el consentimiento para transferencias debe seguir pidiéndose expreso, y el plazo de 5 días para subsanar una solicitud ARCO incompleta que arco_formato_respuesta.md atribuye al Art. 29: el Art. 28 vigente (requisitos de la solicitud) no trae ese plazo, así que no se renumeró. La nota 'Producto completo: 8 de 8 skills (plugin v0.6.0)' de arriba es anterior y no se revisó en esta versión.
