# Plantilla — Documento de Seguridad de Datos Personales

> Estructurada conforme al Art. 61 del Reglamento de la LFPDPPP: las nueve acciones que el responsable deberá considerar para la seguridad de los datos (Fracc. I a IX) y la relación de las medidas de seguridad que exige su último párrafo. El Art. 60 del Reglamento fija los factores para determinar esas medidas. "Documento de seguridad" es el nombre práctico de este expediente: ni la ley ni el Reglamento usan esa expresión.

---

# DOCUMENTO DE SEGURIDAD DE DATOS PERSONALES

**Responsable:** [DENOMINACIÓN]
**RFC:** [RFC]
**Domicilio:** [DOMICILIO]
**Fecha de elaboración:** [DD/MM/AAAA]
**Fecha de última actualización:** [DD/MM/AAAA]
**Versión:** [1.0]
**Aprobado por:** [Nombre y cargo de quien aprueba por el Responsable]

---

## 1. Introducción y alcance

El presente Documento de Seguridad establece las medidas administrativas, físicas y técnicas que [Responsable] implementa para proteger los Datos Personales que trata, conforme al Art. 18 LFPDPPP y a los Arts. 57 a 62 de su Reglamento.

**Aplicación:** Este documento es de observancia obligatoria para todo el personal de [Responsable], así como para los Encargados, que tratan Datos Personales por cuenta del Responsable (Art. 2 Fracc. XII LFPDPPP), en los términos de las cláusulas contractuales u otro instrumento jurídico que los vincule (Art. 51 Reglamento).

---

## 2. Inventario de Datos Personales y Sistemas de Tratamiento

*Elemento obligatorio (Art. 61 Fracc. I Reglamento)*

A continuación se presenta el inventario de las bases de datos personales que trata el Responsable. (Ver detalle completo en el Anexo "Inventario de Datos Personales"). Las filas de la tabla son ejemplos: sustitúyalas por las bases reales del Responsable.

**Cómo se lee la última columna.** "Nivel de riesgo" es el resultado de la matriz probabilidad × impacto de la sección 4.1 y sirve para priorizar el plan de trabajo; no es el nivel de medidas que corresponde a la base. Toda base que contenga datos sensibles —los de salud, incluidos los exámenes médicos de ingreso y el antidoping, y los psicométricos en lo que revelen datos sensibles (Art. 2 fracc. VI LFPDPPP); por criterio prudencial, también los biométricos— se protege con medidas de nivel alto (cifrado, control de acceso reforzado, bitácoras y segregación de funciones) aunque su celda de riesgo resulte Media o Baja, porque las medidas se determinan tomando en cuenta la sensibilidad de los datos y las posibles consecuencias para las personas titulares (Art. 18, segundo párrafo, LFPDPPP; Art. 60 del Reglamento). Al calificar el impacto de una base con datos sensibles, no lo fije por debajo de Alto.

| Sistema/Base | Área responsable | Tipo de datos | Sensibles | Cantidad aprox. titulares | Ubicación | Nivel de riesgo |
|--------------|------------------|---------------|-----------|---------------------------|-----------|-----------------|
| [Sistema de Nómina] | [RH] | Identificación, contacto, laborales, financieros, biométricos | Sí (biométricos, por criterio prudencial) | [#] | [Servidor local + nube] | Medio |
| [CRM Clientes] | [Ventas] | Identificación, contacto, comerciales | No | [#] | [Nube] | Bajo |
| [Expedientes Físicos RH] | [RH] | Identificación, laborales, contractuales | Sí (cuando aplique) | [#] | [Archivo físico] | Bajo |
| [Sistema Contable] | [Contabilidad] | Identificación de clientes, datos fiscales y bancarios | No | [#] | [Servidor local] | Medio |
| [Lista de Proveedores] | [Compras] | Identificación, contacto, fiscales | No | [#] | [Archivos compartidos + carpeta física] | Bajo |
| [Candidatos en proceso] | [RH] | Identificación, contacto, académicos, psicométricos | Sí (psicométricos) | [#] | [Nube] | Bajo |
| [Cámaras de seguridad] | [Seguridad] | Imágenes de video | No por sí mismas (sin reconocimiento facial) | [#] | [NVR local] | Bajo |
| [Lista de visitantes] | [Recepción] | Identificación, contacto | No | [#] | [Físico + digital] | Bajo |

### 2.1 Registro de medios de almacenamiento

*Elemento obligatorio (Art. 61 Fracc. IX Reglamento)*

Soportes físicos y electrónicos (Art. 2 Fracc. X y XI Reglamento) en los que se guardan los Datos Personales del inventario:

| Medio o soporte | Tipo | Bases que contiene | Ubicación | Custodio | ¿Cifrado? | Baja segura |
|-----------------|------|--------------------|-----------|----------|-----------|-------------|
| [Servidor local] | Electrónico | [Nómina, Sistema Contable, Lista de Proveedores (archivos compartidos), Lista de visitantes (Excel)] | [Oficina] | [TI] | [Sí/No] | [Borrado seguro] |
| [Nube: proveedor y país] | Electrónico | [CRM Clientes, Nómina, Candidatos en proceso (ATS), respaldos en la nube] | [País] | [TI] | [Sí/No] | [Supresión certificada por el proveedor] |
| [Archivero con llave] | Físico | [Expedientes Físicos RH] | [Oficina RH] | [RH] | No aplica | [Trituración] |
| [Carpetas y cuadernos de trabajo] | Físico | [Lista de Proveedores (carpeta), Lista de visitantes (cuaderno)] | [Compras, Recepción] | [Compras, Recepción] | No aplica | [Trituración] |
| [Grabador de video (NVR)] | Electrónico | [Cámaras de seguridad] | [Sala de monitoreo] | [Seguridad] | [Sí/No] | [Sobreescritura cíclica; destrucción física del disco al darlo de baja] |
| [Discos o USB de respaldo] | Electrónico | [Respaldos] | [Resguardo] | [TI] | [Sí/No] | [Destrucción física] |
| [Otros] | | | | | | |

---

## 3. Funciones y obligaciones de las personas que tratan Datos Personales

*Elemento obligatorio (Art. 61 Fracc. II Reglamento)*

### 3.1 Estructura organizacional para protección de datos

**Persona o departamento de datos personales (Art. 29 LFPDPPP):**
- Nombre: [nombre]
- Cargo: [cargo]
- Correo: [correo]
- Funciones:
  - Dar trámite a las solicitudes ARCO (función que le asigna el Art. 29 LFPDPPP; las demás de esta lista las asigna el Responsable)
  - Mantener actualizado este Documento de Seguridad
  - Coordinar la capacitación del personal
  - Servir de enlace con la Secretaría Anticorrupción y Buen Gobierno
  - Coordinar la respuesta a vulneraciones de seguridad

**Comité de Privacidad (opcional para organizaciones grandes):**
- Integrantes: [áreas]
- Funciones: aprobar políticas, revisar incidentes graves, autorizar transferencias relevantes

### 3.2 Obligaciones del personal

Todo el personal que tenga acceso a Datos Personales debe:

a) Tratar los datos únicamente conforme a sus funciones autorizadas
b) Guardar absoluta confidencialidad sobre los datos a los que tenga acceso, aun después de terminar su relación con el Responsable (Art. 20 LFPDPPP)
c) Aplicar las medidas de seguridad establecidas en este documento
d) Reportar inmediatamente a la persona o departamento de datos personales cualquier incidente o vulneración
e) Participar en las capacitaciones obligatorias en materia de protección de datos
f) Firmar y respetar el Convenio de Confidencialidad y Tratamiento de Datos Personales

### 3.3 Matriz de roles y accesos

| Rol/Puesto | Datos a los que accede | Operaciones autorizadas | Nivel de acceso |
|------------|------------------------|------------------------|-----------------|
| Director General | Todos | Consulta | Total |
| Gerente RH | Empleados | Consulta, modificación | Total a RH |
| Auxiliar contable | Clientes y proveedores (fiscales) | Consulta, modificación | Limitado a contabilidad |
| Sistemas/TI | Bases de datos completas | Administrar (no operar) | Técnico/admin |
| Ventas | Clientes | Consulta, modificación | Cartera asignada |
| [Otros] | | | |

---

## 4. Análisis de Riesgos

*Elemento obligatorio (Art. 61 Fracc. III Reglamento)*

### 4.1 Metodología

Se aplica una matriz de probabilidad × impacto sobre los activos identificados en el inventario, considerando:

- **Probabilidad:** baja (1), media (2), alta (3)
- **Impacto:** bajo (1), medio (2), alto (3)
- **Riesgo:** producto de ambos (1-3 bajo, 4-6 medio, 7-9 alto)

Con el resultado, las medidas de seguridad se determinan considerando los factores del Art. 18 LFPDPPP y del Art. 60 del Reglamento: riesgo inherente por tipo de dato, sensibilidad de los datos, desarrollo tecnológico y posibles consecuencias de una vulneración para los titulares; además, se procura tomar en cuenta el número de titulares, las vulnerabilidades previas en los sistemas de tratamiento, el valor de los datos para un tercero no autorizado y los demás factores que puedan incidir en el nivel de riesgo o que resulten de otras leyes o regulación aplicable al Responsable. Conforme al Art. 18 LFPDPPP, el Responsable no adoptará medidas de seguridad menores a aquellas que mantenga para el manejo de su información.

### 4.2 Riesgos identificados

| ID | Activo | Amenaza | Probabilidad | Impacto | Riesgo | Tratamiento |
|----|--------|---------|--------------|---------|--------|-------------|
| R-01 | Sistema de Nómina | Acceso no autorizado | Media (2) | Alto (3) | 6 (Medio) | Mitigar |
| R-02 | Expedientes físicos RH | Robo o extravío | Baja (1) | Alto (3) | 3 (Bajo) | Mitigar |
| R-03 | Correo institucional | Phishing/ingeniería social | Alta (3) | Medio (2) | 6 (Medio) | Mitigar |
| R-04 | Respaldos en la nube | Fuga por proveedor | Baja (1) | Alto (3) | 3 (Bajo) | Aceptar con controles |
| R-05 | Dispositivos móviles | Pérdida o robo | Media (2) | Medio (2) | 4 (Medio) | Mitigar |
| R-06 | Personal interno | Uso indebido por insider | Baja (1) | Alto (3) | 3 (Bajo) | Mitigar |
| R-07 | Sitio web | Inyección SQL / brecha | Media (2) | Alto (3) | 6 (Medio) | Mitigar |
| [R-XX] | [otros] | | | | | |

### 4.3 Conclusión del análisis

[Resumen del nivel global de riesgo y áreas que requieren mayor atención]

---

## 5. Medidas de seguridad y análisis de brecha

*Elemento obligatorio (Art. 61 Fracc. IV y V Reglamento)*

Estas tablas, mantenidas al día junto con las medidas por base del Anexo A, forman la relación de las medidas de seguridad que exige el último párrafo del Art. 61 del Reglamento y se actualizan en los supuestos de la sección 7.1. Por cada medida aplicable se indica si está implementada de manera efectiva (Fracc. IV) y la brecha entre las existentes y las faltantes necesarias (Fracc. V):

### Medidas administrativas

| Medida | Implementada | Brecha | Prioridad |
|--------|--------------|--------|-----------|
| Política de protección de datos | [Sí/No/Parcial] | [Descripción] | [Alta/Media/Baja] |
| Convenios de confidencialidad firmados por personal | [Sí/No/Parcial] | | |
| Programa de capacitación documentado | [Sí/No/Parcial] | | |
| Procedimiento ARCO formalizado | [Sí/No/Parcial] | | |
| Bitácora de solicitudes ARCO | [Sí/No/Parcial] | | |
| Protocolo de vulneraciones | [Sí/No/Parcial] | | |
| Contratos con encargados con cláusulas LFPDPPP | [Sí/No/Parcial] | | |

### Medidas físicas

| Medida | Implementada | Brecha | Prioridad |
|--------|--------------|--------|-----------|
| Control de acceso a oficinas | [Sí/No/Parcial] | | |
| Gabinetes con llave para expedientes físicos | [Sí/No/Parcial] | | |
| Destrucción segura de papel (trituradora) | [Sí/No/Parcial] | | |
| Cámaras de seguridad | [Sí/No/Parcial] | | |
| Custodia de medios físicos (USB, discos) | [Sí/No/Parcial] | | |

### Medidas técnicas

| Medida | Implementada | Brecha | Prioridad |
|--------|--------------|--------|-----------|
| Contraseñas robustas y rotación | [Sí/No/Parcial] | | |
| Autenticación multifactor (MFA) | [Sí/No/Parcial] | | |
| Cifrado de datos sensibles en reposo | [Sí/No/Parcial] | | |
| Cifrado en tránsito (HTTPS, VPN) | [Sí/No/Parcial] | | |
| Antivirus y firewall actualizados | [Sí/No/Parcial] | | |
| Respaldos verificados periódicamente | [Sí/No/Parcial] | | |
| Bitácoras de acceso a sistemas críticos | [Sí/No/Parcial] | | |
| Actualizaciones de seguridad (patching) | [Sí/No/Parcial] | | |

---

## 6. Plan de trabajo

*Elemento obligatorio (Art. 61 Fracc. VI Reglamento)*

Para cubrir las brechas identificadas:

| Acción | A cargo de | Recursos | Fecha objetivo | Estatus |
|--------|-------------|----------|----------------|---------|
| [Implementar MFA en sistemas críticos] | TI | [Presupuesto] | [DD/MM/AAAA] | [Pendiente] |
| [Adquirir trituradora industrial] | Administración | [$] | [DD/MM/AAAA] | [Pendiente] |
| [Capacitar al personal en LFPDPPP] | Persona o departamento de datos personales | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Formalizar contratos con encargados] | Jurídico | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Cifrar respaldos de nómina] | TI | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Implementar bitácora ARCO digital] | Persona o departamento de datos personales | [$] | [DD/MM/AAAA] | [Pendiente] |
| [Otras acciones] | | | | |

---

## 7. Mecanismos de monitoreo y revisión

*Elemento obligatorio (Art. 61 Fracc. VII Reglamento: revisiones o auditorías)*

### 7.1 Revisión periódica del Documento de Seguridad

- **Frecuencia:** Anual y cuando ocurra alguno de los siguientes eventos:
  - Cambios a las medidas o procesos de seguridad por mejora continua (Art. 62 Fracc. I Reglamento)
  - Modificación sustancial de procesos o del tratamiento que cambie el nivel de riesgo (Art. 62 Fracc. II Reglamento)
  - Implementación de nuevos sistemas que traten datos personales
  - Reforma legal aplicable
  - Cualquier vulneración de los sistemas de tratamiento u otra afectación a los datos personales, aunque no afecte de forma significativa al titular (Art. 62 Fracc. III y IV Reglamento)
- **A cargo de la revisión:** Persona o departamento de datos personales
- **Aprobación de la actualización:** [instancia interna que aprueba, p. ej., Dirección General]

### 7.2 Auditorías internas

- **Frecuencia:** Anual
- **Alcance:** Verificación del cumplimiento de las medidas establecidas
- **A cargo de:** [Área de auditoría / consultor externo / persona o departamento de datos personales]
- **Entregable:** Reporte de auditoría con hallazgos y recomendaciones

### 7.3 Indicadores de cumplimiento

- Número de solicitudes ARCO recibidas y atendidas en plazo
- Número de vulneraciones reportadas y atendidas
- Porcentaje de personal capacitado en el año
- Porcentaje de proveedores con contrato actualizado

---

## 8. Programa de Capacitación

*Elemento obligatorio (Art. 61 Fracc. VIII Reglamento)*

### 8.1 Capacitación inicial

Todo nuevo personal con acceso a Datos Personales recibirá, dentro de los primeros 30 días de su ingreso:

- Inducción general en LFPDPPP (1-2 horas)
- Capacitación específica en sus funciones
- Firma del Convenio de Confidencialidad

### 8.2 Capacitación periódica

- **Frecuencia:** Anual mínimo, o cuando haya cambios relevantes
- **Modalidad:** [Presencial / en línea / mixta]
- **Contenido mínimo:**
  - Conceptos básicos y derechos ARCO
  - Medidas de seguridad aplicables al puesto
  - Identificación y reporte de vulneraciones
  - Casos prácticos del sector

### 8.3 Registro de capacitación

Se llevará bitácora de:
- Fecha y modalidad
- Participantes (con firma o registro digital)
- Contenidos cubiertos
- Evaluación de comprensión

---

## 9. Anexos

- Anexo A: Inventario de Datos Personales (detalle completo)
- Anexo B: Convenio de Confidencialidad (modelo para personal)
- Anexo C: Procedimiento ARCO
- Anexo D: Protocolo de Vulneraciones
- Anexo E: Matriz de Roles y Accesos detallada
- Anexo F: Listado de proveedores con tratamiento de datos

*Nota para quien llena la plantilla (bórrela del documento final): de esta lista hay plantilla del Anexo A (inventario) y del Anexo D (protocolo de vulneraciones); el Anexo C se arma con el procedimiento ARCO y los formatos de solicitud y de respuesta. El Convenio de Confidencialidad (B), la matriz detallada de roles y accesos (E) y el listado de proveedores (F) los elabora el Responsable. Deje en la lista únicamente los anexos que acompañen al documento al momento de aprobarlo; quite los que falten y regístrelos como acción en el plan de trabajo de la sección 6, con persona a cargo y fecha. Si el Anexo B todavía no existe, revise también los incisos 3.2 f) y 8.1, que obligan al personal a firmarlo.*

---

**Firma del Responsable:**

___________________________________________
[Nombre y cargo del representante legal]

**Firma de la persona o departamento de datos personales:**

___________________________________________
[Nombre y cargo de quien firma por la persona o departamento de datos personales]

**Fecha de aprobación:** [DD/MM/AAAA]

---

*Generado con apoyo de NexFiscal.app — Compliance LFPDPPP v1.0*
*Este documento es interno y debe mantenerse en custodia controlada.*
