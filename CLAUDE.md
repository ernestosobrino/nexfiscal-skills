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

**Plugin 0.9.4 (11-sep-2026):** limpieza de la numeración de la ley abrogada de 2010 en compliance-lfpdppp y contratos-mercantiles, contra una concordancia 2010→2025 verificada en el texto vigente de Diputados y en el DOF del 20-03-2025 (no contra la propia skill): aviso Art. 17→16, gratuidad ARCO 35→34, transferencias 37→36 y 36→35, negativa ARCO Art. 33, plazos Art. 31, requisitos de la solicitud Art. 29→28; la autoridad ya no es el INAI sino la Secretaría Anticorrupción y Buen Gobierno; y la ley abrogada tenía 6 fracciones en el aviso, no 11. "Persona o departamento de datos personales" en lugar de "encargado" se corrigió SOLO en el comparativo LGPDPPSO. En la 0.9.5 quedó bien el SKILL.md; siguen 22 lugares en plantillas que llaman "Encargado" a la figura del Art. 29 (en la ley el encargado es quien trata datos por cuenta del responsable). Pendiente.

**Plugin 0.9.5 (11-sep-2026, visto bueno de Ernesto):** lo que cambia la asesoría, con fundamento verificado en la ley vigente y en el Reglamento de 2011 (sigue aplicando en lo que no se oponga): la cláusula de aceptación de transferencias es OBLIGATORIA (Art. 35); los mecanismos de revocación también (Art. 7); consentimiento para transferencias tácito por regla general, expreso para datos financieros o patrimoniales (Art. 7) y expreso y por escrito para sensibles (Art. 8); el aviso simplificado es el exigible en medios electrónicos, ópticos, sonoros o visuales (Art. 16 fracc. II) y el corto solo es remisión adicional —los modelos de cookies, CCTV, app y llamada ya traen su mínimo, y el de cookies distingue las finalidades que requieren consentimiento—; los datos sensibles no se recaban por medios sin firma ni autenticación; requerimiento ARCO: el titular tiene 10 días hábiles, no 5 (Art. 96 del Reglamento; la plantilla le quitaba la mitad del plazo); requisitos de la solicitud con las 5 fracciones del Art. 28 y la excepción del acceso; definiciones del Art. 2 con la redacción de 2025. Revisión adversarial contra los textos oficiales antes de publicar.

**Pendientes para la 0.9.6** (detectados en esa revisión, fuera de lo aprobado): el Art. 40 no pone plazo de 15 días cuando el responsable no contesta y la skill dice que sí (puede hacer creer al titular que perdió su derecho); los elementos del documento de seguridad están en el Art. 61 del Reglamento, no en el 60; redes sociales públicas sí requieren aviso; cancelar no exige motivo (Art. 24); el "Encargado" de arriba; capacitar al personal no es solo buena práctica (Reglamento Art. 61 fracc. VIII); precisar receptores y finalidades de cada transferencia; y en aviso_empleados.md, la fila de la aseguradora debe decir "No, Art. 36 fracc. IV (contrato en interés del trabajador)" en lugar de "Por participar en el beneficio". La nota 'Producto completo: 8 de 8 skills (plugin v0.6.0)' de arriba es anterior y no se revisó.
