# Plantilla — Inventario de Datos Personales

> Componente del Documento de Seguridad (Art. 61 Fracc. I Reglamento LFPDPPP; la sección Almacenamiento alimenta el registro de medios de almacenamiento, Art. 61 Fracc. IX Reglamento). Inventario completo de todas las bases de datos personales que trata el Responsable.

---

# INVENTARIO DE DATOS PERSONALES

**Responsable:** [DENOMINACIÓN]
**Fecha de elaboración:** [DD/MM/AAAA]
**Fecha de última actualización:** [DD/MM/AAAA]
**A cargo del inventario:** [Persona o departamento de datos personales]

---

## Instrucciones

Por cada **base de datos, sistema o conjunto de información** que trate datos personales (digital o físico), completar la ficha siguiente. Incluir bases que sean parte de procesos rutinarios (nómina, clientes, expedientes laborales, contabilidad) y bases temporales (campañas, eventos, candidatos).

---

## FICHA TIPO

### Identificación

| Campo | Detalle |
|-------|---------|
| **Nombre de la base/sistema** | [Ej. "Sistema de Nómina ContPAQi"] |
| **Área responsable** | [Recursos Humanos] |
| **Persona a cargo (nombre y cargo)** | [Nombre, cargo] |
| **Fecha de creación** | [DD/MM/AAAA] |
| **¿Activa?** | [Sí / Suspendida / Histórica] |

### Datos contenidos

| Campo | Detalle |
|-------|---------|
| **Categorías de datos** | [Identificación / Contacto / Laborales / Financieros / Académicos / Sensibles] |
| **Lista específica de datos** | [Nombre, RFC, CURP, NSS, salario, fecha ingreso, etc.] |
| **¿Incluye datos sensibles?** | [Sí / No - especificar cuáles] |
| **Origen de los datos** | [Recabados directamente del titular / De terceros / Fuente de acceso público] |
| **¿Cómo se obtuvo el consentimiento?** | [Firma del aviso / Casilla digital / Tácito / No aplica por excepción legal (Art. 9 LFPDPPP)]. El tácito no basta para datos financieros o patrimoniales (expreso, Art. 7 LFPDPPP) ni para sensibles (expreso y por escrito, con firma autógrafa, firma electrónica o mecanismo de autenticación, Art. 8 LFPDPPP) |

### Características operativas

| Campo | Detalle |
|-------|---------|
| **Categorías de titulares** | [Empleados activos / Ex empleados / Clientes / Prospectos / Proveedores / Visitantes] |
| **Cantidad aproximada de registros** | [#] |
| **Finalidad(es) del tratamiento** | [Listar - primarias y secundarias por separado] |
| **Tiempo de conservación previsto** | [Periodo y fundamento] |
| **Procedimiento de bloqueo y supresión** | [Descripción breve] |

### Almacenamiento

| Campo | Detalle |
|-------|---------|
| **Tipo** | [Digital / Físico / Mixto] |
| **Ubicación física** | [Oficina, archivero, área restringida] |
| **Ubicación lógica** | [Servidor on-premise / Nube (proveedor y país) / Disco local] |
| **¿Está cifrada?** | [Sí (algoritmo) / No / Parcial] |
| **¿Hay respaldos?** | [Sí - frecuencia y ubicación / No] |

### Accesos

| Rol/Puesto | Operaciones autorizadas | Justificación |
|------------|------------------------|---------------|
| | | |
| | | |

### Transferencias (a terceros distintos del encargado; Art. 2 Fracc. XX LFPDPPP)

| Destinatario | Finalidad | ¿Requiere consentimiento? | Documento que respalda |
|--------------|-----------|---------------------------|------------------------|
| | | | |

### Encargados (proveedores que tratan los datos por cuenta del Responsable: remisión, no transferencia)

| Proveedor | Servicio | ¿Contrato con cláusulas? | Vigencia |
|-----------|----------|--------------------------|----------|
| | | | |

### Medidas de seguridad específicas

| Tipo | Descripción |
|------|-------------|
| **Administrativas** | [Convenios de confidencialidad firmados, control de accesos por roles, capacitación específica] |
| **Físicas** | [Llaves, cámaras, áreas restringidas] |
| **Técnicas** | [MFA, cifrado, logs, antivirus, segregación de red] |

### Análisis de riesgo

| Campo | Detalle |
|-------|---------|
| **Probabilidad de incidente** | [Baja / Media / Alta] |
| **Impacto si ocurre** | [Bajo / Medio / Alto] |
| **Nivel de riesgo** | [Producto de los dos, con la escala de la sección 4.1 del Documento de Seguridad] |
| **Tratamiento de riesgo** | [Mitigar / Aceptar / Transferir / Evitar] |

### Observaciones / notas

[Cualquier consideración relevante, normativa sectorial aplicable, particularidades del sistema, etc.]

---

## RESUMEN — TABLA MAESTRA DE BASES DE DATOS

| ID | Nombre base | Área | Tipo datos | Sensibles | # titulares | Almacenamiento | Riesgo |
|----|-------------|------|-----------|-----------|-------------|----------------|--------|
| BD-01 | Sistema de Nómina | RH | Identif., laborales, financieros, biométricos | Sí (biométricos, por criterio prudencial) | [#] | Servidor local + nube | Medio |
| BD-02 | CRM Clientes | Ventas | Identif., contacto, comercial | No | [#] | Nube | Bajo |
| BD-03 | Expedientes Físicos RH | RH | Identif., laborales, contractuales | Sí (cuando aplique) | [#] | Archivo físico | Bajo |
| BD-04 | Sistema Contable | Contab. | Identif., fiscales, bancarios | No | [#] | Servidor local | Medio |
| BD-05 | Proveedores | Compras | Identif., contacto, fiscales | No | [#] | Archivos compartidos + carpeta física | Bajo |
| BD-06 | Candidatos en proceso | RH | Identif., contacto, académicos, psicométricos | Sí (psicométricos) | [#] | Nube | Bajo |
| BD-07 | Cámaras de seguridad | Seguridad | Imágenes de video | No por sí mismas (sin reconocimiento facial) | [#] | NVR local | Bajo |
| BD-08 | Lista de visitantes | Recepción | Identif., contacto | No | [#] | Físico + digital | Bajo |
| [BD-XX] | [otros] | | | | | | |

---

## Revisión y actualización

| Fecha | Cambios realizados | Realizado por |
|-------|--------------------|---------------|
| [DD/MM/AAAA] | Creación inicial | [Nombre] |
| | | |

---

*Generado con apoyo de NexFiscal.app — Compliance LFPDPPP v1.0*
*Este inventario es interno y debe mantenerse en custodia controlada por la persona o departamento de datos personales.*
