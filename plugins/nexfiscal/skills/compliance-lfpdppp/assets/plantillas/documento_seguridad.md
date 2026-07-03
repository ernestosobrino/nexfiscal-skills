# Plantilla — Documento de Seguridad de Datos Personales

> Cumple con el Art. 60 del Reglamento de la LFPDPPP. Contiene los 7 elementos obligatorios.

---

# DOCUMENTO DE SEGURIDAD DE DATOS PERSONALES

**Responsable:** [DENOMINACIÓN]
**RFC:** [RFC]
**Domicilio:** [DOMICILIO]
**Fecha de elaboración:** [DD/MM/AAAA]
**Fecha de última actualización:** [DD/MM/AAAA]
**Versión:** [1.0]
**Aprobado por:** [Nombre y cargo del responsable]

---

## 1. Introducción y alcance

El presente Documento de Seguridad establece las medidas administrativas, físicas y técnicas que [Responsable] implementa para proteger los Datos Personales que trata, conforme al Art. 19 LFPDPPP y al Art. 60 de su Reglamento.

**Aplicación:** Este documento es de observancia obligatoria para todo el personal de [Responsable], así como para los Encargados y terceros que tengan acceso a Datos Personales por cuenta del Responsable.

---

## 2. Inventario de Datos Personales y Sistemas de Tratamiento

*Elemento obligatorio (Art. 60 Fracc. I Reglamento)*

A continuación se presenta el inventario de las bases de datos personales que trata el Responsable. (Ver detalle completo en el Anexo "Inventario de Datos Personales").

| Sistema/Base | Área responsable | Tipo de datos | Sensibles | Cantidad aprox. titulares | Ubicación | Nivel de riesgo |
|--------------|------------------|---------------|-----------|---------------------------|-----------|-----------------|
| [Sistema de Nómina] | [RH] | Identificación, contacto, laborales, financieros, biométricos | Sí (biométricos, salud) | [#] | [Servidor local + nube] | Alto |
| [CRM Clientes] | [Ventas] | Identificación, contacto, comerciales | No | [#] | [Nube] | Medio |
| [Expedientes Físicos RH] | [RH] | Identificación, laborales, contractuales | Sí (cuando aplique) | [#] | [Archivo físico] | Medio |
| [Sistema Contable] | [Contabilidad] | Identificación de clientes, datos fiscales y bancarios | No | [#] | [Servidor local] | Medio |
| [Lista de Proveedores] | [Compras] | Identificación, contacto, fiscales | No | [#] | [Archivos compartidos] | Bajo |

---

## 3. Funciones y obligaciones de las personas que tratan Datos Personales

*Elemento obligatorio (Art. 60 Fracc. II Reglamento)*

### 3.1 Estructura organizacional para protección de datos

**Encargado / Departamento de Datos Personales:**
- Nombre: [nombre]
- Cargo: [cargo]
- Correo: [correo]
- Funciones:
  - Atender solicitudes ARCO
  - Mantener actualizado este Documento de Seguridad
  - Coordinar la capacitación del personal
  - Servir de enlace con el INAI
  - Coordinar la respuesta a vulneraciones de seguridad

**Comité de Privacidad (opcional para organizaciones grandes):**
- Integrantes: [áreas]
- Funciones: aprobar políticas, revisar incidentes graves, autorizar transferencias relevantes

### 3.2 Obligaciones del personal

Todo el personal que tenga acceso a Datos Personales debe:

a) Tratar los datos únicamente conforme a sus funciones autorizadas
b) Guardar absoluta confidencialidad sobre los datos a los que tenga acceso
c) Aplicar las medidas de seguridad establecidas en este documento
d) Reportar inmediatamente al Encargado cualquier incidente o vulneración
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

*Elemento obligatorio (Art. 60 Fracc. III Reglamento)*

### 4.1 Metodología

Se aplica una matriz de probabilidad × impacto sobre los activos identificados en el inventario, considerando:

- **Probabilidad:** baja (1), media (2), alta (3)
- **Impacto:** bajo (1), medio (2), alto (3)
- **Riesgo:** producto de ambos (1-3 bajo, 4-6 medio, 7-9 alto)

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

## 5. Análisis de Brecha

*Elemento obligatorio (Art. 60 Fracc. IV Reglamento)*

Comparación entre las medidas existentes y las recomendadas/requeridas:

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

*Elemento obligatorio (Art. 60 Fracc. V Reglamento)*

Para cubrir las brechas identificadas:

| Acción | Responsable | Recursos | Fecha objetivo | Estatus |
|--------|-------------|----------|----------------|---------|
| [Implementar MFA en sistemas críticos] | TI | [Presupuesto] | [DD/MM/AAAA] | [Pendiente] |
| [Adquirir trituradora industrial] | Administración | [$] | [DD/MM/AAAA] | [Pendiente] |
| [Capacitar al personal en LFPDPPP] | Encargado | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Formalizar contratos con encargados] | Jurídico | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Cifrar respaldos de nómina] | TI | Interno | [DD/MM/AAAA] | [Pendiente] |
| [Implementar bitácora ARCO digital] | Encargado | [$] | [DD/MM/AAAA] | [Pendiente] |
| [Otras acciones] | | | | |

---

## 7. Mecanismos de monitoreo y revisión

*Elemento obligatorio (Art. 60 Fracc. VI Reglamento)*

### 7.1 Revisión periódica del Documento de Seguridad

- **Frecuencia:** Anual y cuando ocurra alguno de los siguientes eventos:
  - Modificación sustancial de procesos
  - Implementación de nuevos sistemas que traten datos personales
  - Reforma legal aplicable
  - Vulneración de seguridad significativa
- **Responsable de la revisión:** Encargado de Datos Personales
- **Aprobación de la actualización:** [autoridad indicada]

### 7.2 Auditorías internas

- **Frecuencia:** Anual
- **Alcance:** Verificación del cumplimiento de las medidas establecidas
- **Responsable:** [Área de auditoría / consultor externo / Encargado]
- **Entregable:** Reporte de auditoría con hallazgos y recomendaciones

### 7.3 Indicadores de cumplimiento

- Número de solicitudes ARCO recibidas y atendidas en plazo
- Número de vulneraciones reportadas y atendidas
- Porcentaje de personal capacitado en el año
- Porcentaje de proveedores con contrato actualizado

---

## 8. Programa de Capacitación

*Elemento obligatorio (Art. 60 Fracc. VII Reglamento)*

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

---

**Firma del Responsable:**

___________________________________________
[Nombre y cargo del representante legal]

**Firma del Encargado de Datos Personales:**

___________________________________________
[Nombre]

**Fecha de aprobación:** [DD/MM/AAAA]

---

*Generado con apoyo de NexFiscal.app — Compliance LFPDPPP v1.0*
*Este documento es interno y debe mantenerse en custodia controlada.*
