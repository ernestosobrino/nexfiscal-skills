# Plantilla — Protocolo de Atención a Vulneraciones de Seguridad de Datos Personales

> Cumple con el Art. 20 LFPDPPP y los Arts. 63-66 del Reglamento.

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
c) Notificar al titular cuando exista afectación significativa, sin dilación
d) Documentar el incidente y aplicar medidas correctivas
e) Cumplir con las obligaciones de la LFPDPPP

---

## 2. Definiciones

**Vulneración de seguridad** (Arts. 63-66 Reglamento LFPDPPP): Cualquier evento que comprometa la confidencialidad, integridad o disponibilidad de los datos personales, incluyendo:

a) **Pérdida o destrucción** no autorizada
b) **Robo, extravío o copia** no autorizada
c) **Uso, acceso o tratamiento** no autorizado
d) **Daño, alteración o modificación** no autorizada

**Afectación significativa:** Aquella que pueda afectar los derechos patrimoniales o morales del titular, considerando: sensibilidad de los datos, cantidad de titulares, probabilidad de uso indebido, y consecuencias previsibles.

---

## 3. Roles y responsabilidades

| Rol | Responsable | Función principal |
|-----|-------------|-------------------|
| **Detector** | Cualquier persona del Responsable | Reportar al Encargado dentro de 1 hora desde la detección |
| **Encargado de Datos Personales** | [Nombre/Cargo] | Coordinar la respuesta y notificaciones |
| **TI / Seguridad Informática** | [Nombre/Cargo] | Contención técnica y evidencia digital |
| **Jurídico** | [Nombre/Cargo] | Análisis legal y obligaciones de notificación |
| **Dirección General** | [Nombre/Cargo] | Decisiones de alto nivel y comunicación externa |
| **Comunicación** | [Nombre/Cargo] | Mensajes a titulares y, en su caso, comunicado público |
| **Recursos Humanos** | [Nombre/Cargo] | Si involucra personal interno como responsable |

### 3.1 Activación del equipo de respuesta

Ante el reporte de una posible vulneración, el Encargado convocará al equipo en un plazo no mayor a **2 horas hábiles**. La conformación dependerá del tipo y gravedad del incidente.

---

## 4. Procedimiento de respuesta

### Fase 1 — Detección y reporte (0 a 2 horas)

1. Cualquier persona que detecte un incidente lo reporta inmediatamente al Encargado por:
   - Correo: [correo]
   - Teléfono: [teléfono]
   - Sistema de tickets internos: [si aplica]

2. El Encargado registra el reporte inicial en la **Bitácora de Vulneraciones** con los siguientes datos:
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
- ¿Hay obligación de reportar a autoridad sectorial (CNBV, IFT, COFEPRIS, etc.)?

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

### Fase 4 — Notificación al titular (sin dilación, ideal 72 horas tras confirmación)

**Si hay afectación significativa**, el Responsable notificará a los titulares afectados, conforme al Art. 20 LFPDPPP, mediante un medio idóneo (correo electrónico, comunicación postal, llamada, etc.).

La notificación contendrá:

a) Naturaleza del incidente
b) Datos personales comprometidos
c) Recomendaciones al titular para defender sus derechos
d) Acciones correctivas realizadas
e) Medios para mayor información

Ver formato en la sección 6 de este protocolo.

### Fase 5 — Análisis de causa raíz y medidas correctivas (hasta 30 días)

- Investigación detallada del cómo y por qué del incidente
- Identificación de fallas técnicas, procedimentales o humanas
- Definición de medidas correctivas con responsables y plazos
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

En cumplimiento al Art. 20 de la Ley Federal de Protección de Datos Personales en Posesión de los Particulares, le informamos lo siguiente:

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
- [Monitorear su historial crediticio si datos financieros]
- [Reportar a su banco si se comprometieron datos bancarios]
- [Otras recomendaciones específicas según los datos involucrados]

### Medidas correctivas que hemos implementado

[Listar acciones concretas: cierre de la brecha, refuerzo de seguridad, sanciones internas si aplica, etc.]

### Mayor información

Si tiene preguntas o necesita asistencia, puede contactarnos a:

- Correo: [correo del Encargado]
- Teléfono: [teléfono]
- Página web: [URL]

Lamentamos profundamente lo sucedido y reafirmamos nuestro compromiso con la protección de sus datos personales.

Atentamente,

___________________________________________
[Nombre y cargo del Encargado]
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

Este protocolo se revisará al menos una vez al año y siempre que ocurra un incidente significativo, conforme al Documento de Seguridad.

---

## 9. Capacitación

Todo personal con acceso a datos personales debe conocer este protocolo y saber cómo reportar un incidente. Se incluirá en la capacitación inicial y en los refrescamientos periódicos.

---

*Generado con apoyo de NexFiscal.app — Compliance LFPDPPP v1.0*
*Considere realizar simulacros anuales de respuesta a incidentes para mantener la preparación del equipo.*
