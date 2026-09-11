# Plantilla — Protocolo de Atención a Vulneraciones de Seguridad de Datos Personales

> Estructurada conforme al Art. 19 LFPDPPP y a los Arts. 63-66 del Reglamento (DOF 21-12-2011), que se usa como referencia en lo que no se oponga a la ley vigente.

---

# PROTOCOLO DE ATENCIÓN A VULNERACIONES DE SEGURIDAD

**Responsable:** [DENOMINACIÓN]
**Fecha de elaboración:** [DD/MM/AAAA]
**Versión:** [1.0]
**Aprobado por:** [Nombre y cargo]

---

## 1. Objetivo

Establecer las acciones, roles y plazos que [Responsable] aplicará ante una vulneración de seguridad de datos personales, a efecto de:

a) Contener oportunamente el incidente
b) Evaluar su alcance y afectación
c) Notificar al titular de forma inmediata cuando exista afectación significativa (Art. 19 LFPDPPP)
d) Documentar el incidente y aplicar medidas correctivas
e) Cumplir con las obligaciones de la LFPDPPP

---

## 2. Definiciones

**Vulneración de seguridad** (Art. 63 Reglamento LFPDPPP): La ocurrida en cualquier fase del tratamiento de datos personales que consista en:

a) **Pérdida o destrucción** no autorizada
b) **Robo, extravío o copia** no autorizada
c) **Uso, acceso o tratamiento** no autorizado
d) **Daño, alteración o modificación** no autorizada

**Afectación significativa:** Ni la LFPDPPP ni su Reglamento la definen; el Art. 19 LFPDPPP se refiere a las vulneraciones que afecten de forma significativa los derechos patrimoniales o morales del titular. Como criterio de este protocolo, se valora considerando: sensibilidad de los datos, cantidad de titulares, probabilidad de uso indebido y consecuencias previsibles (ver Fase 3).

---

## 3. Roles y responsabilidades

| Rol | A cargo de | Función principal |
|-----|-------------|-------------------|
| **Detector** | Cualquier persona del Responsable | Reportar a la persona o departamento de datos personales dentro de 1 hora desde la detección |
| **Persona o departamento de datos personales (Art. 29 LFPDPPP)** | [Nombre/Cargo] | Coordinar la respuesta y notificaciones |
| **TI / Seguridad Informática** | [Nombre/Cargo] | Contención técnica y evidencia digital |
| **Jurídico** | [Nombre/Cargo] | Análisis legal y obligaciones de notificación |
| **Dirección General** | [Nombre/Cargo] | Decisiones de alto nivel y comunicación externa |
| **Comunicación** | [Nombre/Cargo] | Mensajes a titulares y, en su caso, comunicado público |
| **Recursos Humanos** | [Nombre/Cargo] | Si el incidente involucra a personal interno como posible causante |

La persona o departamento de datos personales es la figura que el Art. 29 LFPDPPP obliga a designar para dar trámite a las solicitudes de los titulares; encomendarle la coordinación de vulneraciones es decisión interna. La obligación de informar al titular es del Responsable (Art. 19 LFPDPPP).

### 3.1 Activación del equipo de respuesta

Ante el reporte de una posible vulneración, la persona o departamento de datos personales convocará al equipo en un plazo no mayor a **[2 horas]**, aun fuera del horario laboral. La conformación dependerá del tipo y gravedad del incidente.

*Este plazo, y el de 1 hora que la tabla anterior fija al rol Detector, son metas internas que el Responsable decide y puede ajustar a su tamaño y a su horario real de operación, igual que los plazos de las fases de la sección 4: ni la LFPDPPP ni su Reglamento los imponen. Fije únicamente los que pueda sostener.*

---

## 4. Procedimiento de respuesta

Los plazos en horas y días de cada fase son metas internas sugeridas, que el Responsable puede ajustar: ni la LFPDPPP ni su Reglamento fijan plazos para estas fases. Lo que la ley exige es informar al titular de forma inmediata las vulneraciones que afecten de forma significativa sus derechos patrimoniales o morales (Art. 19 LFPDPPP; Art. 64 Reglamento).

### Fase 1 — Detección y reporte (0 a 2 horas)

1. Cualquier persona que detecte un incidente lo reporta inmediatamente a la persona o departamento de datos personales por:
   - Correo: [correo]
   - Teléfono: [teléfono]
   - Sistema de tickets internos: [si aplica]

   Si la vulneración ocurre en sistemas o soportes de un encargado (proveedor que trata datos por cuenta del Responsable), el encargado la notificará al Responsable en los términos y plazos pactados en su contrato (si no los prevé, conviene pactarlos); esa notificación se registra y atiende igual que un reporte interno. Aunque la vulneración ocurra en el encargado, informar al titular corresponde al Responsable (Art. 19 LFPDPPP).

2. La persona o departamento de datos personales registra el reporte inicial en la **Bitácora de Vulneraciones** con los siguientes datos:
   - Fecha y hora del reporte
   - Reportador
   - Descripción inicial
   - Activos potencialmente afectados

3. Se activa el equipo de respuesta según corresponda.

### Fase 2 — Contención (2 a 24 horas)

Acciones inmediatas para detener la propagación del incidente:

- Aislar sistemas comprometidos
- Cambiar credenciales potencialmente afectadas
- Suspender accesos de cuentas sospechosas
- Preservar evidencia digital (logs, configuraciones, copias forenses)
- Si aplica: dar aviso interno restringido para evitar acciones que destruyan evidencia

**Decisiones clave en esta fase:**
- ¿Es necesario activar respaldo o continuidad de negocio?
- ¿Se requiere apoyo externo (consultoría forense, asesoría legal)?
- ¿La regulación aplicable a su sector obliga a reportar el incidente a alguna autoridad? Verifíquelo en las disposiciones de su sector: la LFPDPPP no prevé ese reporte.

### Fase 3 — Evaluación de alcance (24 a 72 horas)

Determinar con precisión:

| Elemento | Información a documentar |
|----------|--------------------------|
| Naturaleza del incidente | Pérdida / robo / acceso no autorizado / etc. |
| Origen / causa probable | Interno / externo / técnico / humano |
| Datos personales comprometidos | Categorías y, si es posible, lista específica |
| ¿Incluye datos sensibles? | Sí / No - cuáles |
| Cantidad estimada de titulares afectados | Número aproximado |
| Periodo de exposición | Desde / hasta |
| Probabilidad de uso indebido | Baja / media / alta |
| Posible afectación a titulares | Patrimonial / moral / discriminación / fraude |

**Determinación de afectación significativa:**

Se considerará afectación significativa cuando concurra al menos uno de los siguientes:

- Datos sensibles comprometidos
- Datos financieros/patrimoniales que permitan fraude o suplantación
- Datos suficientes para suplantación de identidad
- Alta probabilidad de uso indebido por terceros
- Cantidad relevante de titulares afectados

### Fase 4 — Notificación al titular (de forma inmediata, Art. 19 LFPDPPP)

**Si hay afectación significativa**, el Responsable notificará a los titulares afectados, conforme al Art. 19 LFPDPPP, mediante un medio idóneo (correo electrónico, comunicación postal, llamada, etc.). La notificación no espera a que concluya la evaluación de la Fase 3: procede en cuanto se confirme que ocurrió la vulneración y se hayan tomado las acciones encaminadas a detonar la revisión exhaustiva de la magnitud de la afectación, sin dilación alguna (Art. 64 Reglamento).

La notificación contendrá, al menos (Art. 65 Reglamento):

a) Naturaleza del incidente
b) Datos personales comprometidos
c) Recomendaciones al titular sobre las medidas que puede adoptar para proteger sus intereses y defender sus derechos
d) Acciones correctivas realizadas de forma inmediata
e) Medios para mayor información

Ver formato en la sección 6 de este protocolo.

La LFPDPPP y su Reglamento no prevén notificar la vulneración a la Secretaría Anticorrupción y Buen Gobierno: lo que exigen es informar al titular (Art. 19 LFPDPPP). Si alguna norma de su sector exige reportar a otra autoridad, ese reporte se atiende por separado (ver Fase 2).

### Fase 5 — Análisis de causa raíz y medidas correctivas (hasta 30 días)

- Investigación detallada del cómo y por qué del incidente
- Identificación de fallas técnicas, procedimentales o humanas
- Definición de acciones correctivas, preventivas y de mejora, con persona a cargo y plazo para implementarlas (Art. 66 Reglamento)
- Actualización del Análisis de Riesgos y del Documento de Seguridad

### Fase 6 — Documentación y cierre (hasta 60 días)

- Informe final del incidente con cronología, causa raíz, medidas tomadas
- Archivo en la Bitácora de Vulneraciones
- Comunicación de aprendizajes al personal pertinente
- Actualización de capacitación si es necesario

---

## 5. Bitácora de Vulneraciones (formato)

| ID | Fecha detec. | Tipo | Origen | Datos afectados | Titulares afect. | Significativa | Notificación titular | Causa raíz | Medidas correctivas | Cierre |
|----|--------------|------|--------|-----------------|------------------|---------------|----------------------|------------|---------------------|--------|
| V-001 | DD/MM/AAAA | | | | | Sí/No | Fecha | | | DD/MM/AAAA |

---

## 6. Formato de notificación al titular

**[Membrete del Responsable]**

**Lugar y fecha:** [Ciudad, DD/MM/AAAA]
**Asunto:** Notificación sobre incidente de seguridad de datos personales

**C. [NOMBRE DEL TITULAR]**

---

Estimado(a) [Nombre]:

En cumplimiento al Art. 19 de la Ley Federal de Protección de Datos Personales en Posesión de los Particulares, le informamos lo siguiente:

### Naturaleza del incidente

El día [DD/MM/AAAA] se detectó/ocurrió [descripción breve de la naturaleza del incidente: ej. "un acceso no autorizado a nuestros sistemas", "el extravío de un dispositivo que contenía información"], el cual involucra datos personales de los cuales usted es titular.

### Datos personales comprometidos

Los datos que se vieron involucrados en el incidente son:

- [Lista específica de datos: nombre, correo, RFC, etc.]

*(Si aplica:)* **Datos sensibles involucrados:** [especificar].

### Acciones que recomendamos

Para proteger sus derechos, le sugerimos:

- [Cambiar contraseñas relacionadas si aplica]
- [Estar atento a comunicaciones sospechosas]
- [Monitorear su historial crediticio si se comprometieron datos financieros]
- [Reportar a su banco si se comprometieron datos bancarios]
- [Otras recomendaciones específicas según los datos involucrados]

### Medidas correctivas que hemos implementado

[Listar acciones concretas: cierre de la brecha, refuerzo de seguridad, sanciones internas si aplica, etc.]

### Mayor información

Si tiene preguntas o necesita asistencia, puede contactarnos a:

- Correo: [correo de la persona o departamento de datos personales]
- Teléfono: [teléfono]
- Página web: [URL]

Lamentamos profundamente lo sucedido y reafirmamos nuestro compromiso con la protección de sus datos personales.

Atentamente,

___________________________________________
[Nombre y cargo de quien firma por la persona o departamento de datos personales]
[DENOMINACIÓN DEL RESPONSABLE]

---

## 7. Análisis post-incidente

Al concluir la atención del incidente, se realizará una reunión de lecciones aprendidas con el equipo de respuesta y se documentará:

- ¿Qué funcionó bien en la respuesta?
- ¿Qué falló y cómo evitarlo?
- ¿Qué controles preventivos hay que implementar o reforzar?
- ¿La capacitación al personal fue suficiente?
- ¿El protocolo requiere actualización?

---

## 8. Revisión periódica

Este protocolo se revisará al menos una vez al año y siempre que ocurra una vulneración de seguridad u otra afectación a los datos personales, junto con la actualización de la relación de las medidas de seguridad del Documento de Seguridad (sección 7.1 de ese documento; Art. 62 fracc. III y IV Reglamento).

---

## 9. Capacitación

Todo personal con acceso a datos personales debe conocer este protocolo y saber cómo reportar un incidente. Se incluirá en la capacitación inicial y en los refrescamientos periódicos.

---

*Generado con apoyo de NexFiscal.app — Compliance LFPDPPP v1.0*
*Considere realizar simulacros anuales de respuesta a incidentes para mantener la preparación del equipo.*
