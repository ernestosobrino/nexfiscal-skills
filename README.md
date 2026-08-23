<img src="assets/nexfiscal-skills-logo.svg" alt="NexFiscal Skills" width="340">

# NexFiscal Skills

Skills fiscales, laborales y legales para contadores en México, para usar dentro de Claude (claude.ai). Los valores fiscales vigentes (UMA, tablas ISR, cuotas IMSS, INPC…) y todos los cálculos se obtienen en línea del backend NexFiscal a través del connector incluido — con una suscripción activa, tus resultados siempre usan los valores del día, sin descargar ni actualizar nada.

## Instalación (requiere plan de pago de Claude: Pro, Max, Team o Enterprise)

1. En claude.ai: **Customize → Plugins → Personal plugins → “+” → Add marketplace → Add from a repository**.
2. Pega la URL de este repositorio.
3. Instala el plugin **nexfiscal** y autoriza el connector con tu cuenta de suscriptor NexFiscal.

> **Al instalar, Claude te mostrará un aviso de seguridad** indicando que el
> plugin incluye un connector (servidor MCP) externo. Es normal y esperado: ese
> servidor es justamente el que entrega los valores fiscales vigentes. Abajo
> está el detalle exacto de qué hace y qué no hace el plugin.

## Qué hace (y qué NO hace) este plugin — transparencia

Este repositorio contiene **únicamente archivos de texto y datos** (`.md`, `.json`,
`.csv`): las instrucciones de las skills, plantillas de documentos y catálogos.
Puedes revisarlo completo — es público.

**Lo que el plugin NO hace:**

- ❌ **No ejecuta código** en tu equipo: no incluye scripts, binarios ni programas.
- ❌ **No declara hooks ni permisos especiales** (nada corre por su cuenta).
- ❌ **No accede a tus archivos**, tu terminal ni tu sistema.
- ❌ **No instala nada** fuera de Claude.

**Lo que sí hace:**

- ✅ Incluye un **connector (servidor MCP)** que apunta a `https://mcp.nexfiscal.app`,
  operado por NexFiscal, siempre sobre HTTPS.
- ✅ Cuando pides un cálculo, envía a ese servidor **solo los parámetros necesarios**
  (montos, fechas, régimen, RFC a verificar en las listas del SAT) y recibe el
  resultado con su fundamento legal. **No envía tus conversaciones completas.**
- ✅ Requiere tu **clave de suscriptor** para responder; sin suscripción activa las
  skills lo advierten y no entregan cifras.

**Sobre tus datos:** el servidor procesa los parámetros para resolver el cálculo y
registra el uso por herramienta (para soporte y métricas). No vendemos ni
compartimos datos. Dudas: hola@nexfiscal.mx

## Suscripción

El contenido fiscal cambia todo el año (RMF, UMA, tablas ISR, INPC, listas SAT). La suscripción garantiza que cada cálculo use los valores vigentes con su fundamento legal. Sin suscripción activa, las skills lo advierten y no entregan cifras como válidas.

Información y contratación: https://skills.nexfiscal.mx

## Skills incluidas

- **Calculadora de Nómina MX** — nómina, finiquito, costo del trabajador y consulta de valores vigentes e históricos.
- **Actualización y Recargos** — actualización Art. 17-A CFF, recargos por mora (SAT/IMSS/INFONAVIT), parcialidades y pago diferido, saldos a favor, con INPC y tasas en vivo.
- **Régimen Fiscal Óptimo** — comparativo de carga fiscal entre RESICO, Actividad Empresarial, arrendamiento, plataformas y personas morales, con tablas, topes y costos vigentes.
- **Dictaminador CFDI** — validación de facturas electrónicas con catálogos del Anexo 20 y verificación de RFCs en las **listas 69 / 69-B / 69-B Bis y la nueva 49 Bis (CFDI falsos, vigente 2026) del SAT en vivo**, con fecha de corte.
- **Conciliador IMSS/INFONAVIT** — concilia la EMA mensual y la EBA bimestral contra la determinación del SUA, y explica cada diferencia con su causa y fundamento: incapacidades o ausentismo no reflejados (Art. 31 LSS), salario base distinto, tope de 25 UMA, prima de riesgo o tasa CEAV de otro ejercicio.
- **Gestor Laboral MX** — documentos y procesos laborales conforme a la LFT.
- **Contratos Mercantiles** — redacción de contratos mercantiles mexicanos.
- **Redactor de Actas de Asambleas** — actas y resoluciones societarias.
- **Compliance LFPDPPP** — avisos de privacidad y cumplimiento de datos personales.

---

*Los cálculos son informativos y no sustituyen la opinión de un profesional fiscal o laboral.*
