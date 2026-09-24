# Laboratorio: Implementación y Análisis de Controles de Seguridad (Caso de Estudio Escolar)

## 📌 Descripción del Proyecto
Este repositorio documenta el análisis de seguridad y la propuesta de arquitectura de controles para el sistema de escuelas públicas de Greenville. Partiendo de un escenario real con múltiples vulnerabilidades e incidentes (como manipulación de calificaciones por parte de alumnos, accesos físicos no autorizados, ataques de ransomware, phishing y desconexión accidental de servidores), se clasifican e implementan medidas basadas en la matriz de **controles de seguridad (Físicos, Técnicos y Administrativos)** y sus **funciones (Preventivos, Detectivos y Correctivos)**.

---

## 🎯 Objetivos
* Analizar las necesidades de seguridad y los puntos vulnerables en una infraestructura distribuida (red de fibra óptica, centro de datos centralizado y aulas).
* Clasificar y proponer medidas defensivas utilizando el modelo de **Defensa en Profundidad (Defense-in-Depth)**.
* Mitigar incidentes específicos documentados en el caso de estudio:
  * Brechas de credenciales y alteración de registros académicos por estudiantes.
  * Accesos físicos no autorizados a zonas sensibles (servidores en bibliotecas o salas de cómputo).
  * Caídas de sistemas por ransomware y ataques de ingeniería social (phishing al personal administrativo).

---

## 🛠️ Taxonomía de Controles de Seguridad

### Tipos de Control:
1. **Controles Físicos:** Restringen y controlan el acceso físico a personas, instalaciones, equipos y servidores (ej. cerraduras biométricas, cámaras CCTV, gabinetes seguros).
2. **Controles Técnicos:** Protegen los sistemas de hardware, software y los datos en tránsito o reposo (ej. autenticación multifactor, cifrado, firewalls, ACLs).
3. **Controles Administrativos:** Políticas, procedimientos, normativas y pautas de concientización que el personal debe cumplir (ej. políticas de contraseñas, capacitación contra phishing).

### Funciones de los Controles:
* **Preventivos:** Detienen las amenazas antes de que ocurran.
* **Detectivos:** Identifican actividades no autorizadas o comportamientos sospechosos en tiempo real.
* **Correctivos:** Restauran los sistemas a un estado normal de la CIA (Confidencialidad, Integridad y Disponibilidad) tras un incidente.

---

## 📊 Propuesta de Controles para el Caso de Estudio (Escuela Greenville)

### 1. Controles Físicos
* **Preventivos:** Instalación de gabinetes de servidores con llave en la biblioteca y control de acceso biométrico o por tarjeta en el centro de datos principal para evitar que personal ajeno (como limpieza) desconecte equipos.
* **Detectivos:** Sistemas de cámaras de seguridad (CCTV) con monitoreo activo y sensores de movimiento en áreas críticas.
* **Correctivos:** Sistemas de respaldo de energía físico (UPS) y protocolos de recuperación rápida ante daños de infraestructura.

### 2. Controles Técnicos
* **Preventivos:** Implementación de Autenticación Multifactor (MFA) obligatoria para el plantel docente y administrativo, evitando que credenciales robadas permitan el acceso a la red de gestión. Segmentación de red (VLANs) para aislar las computadoras de los estudiantes de las terminales administrativas.
* **Detectivos:** Herramientas de detección de intrusos (IDS), auditoría de logs y alertas ante cambios no autorizados en bases de datos académicas.
* **Correctivos:** Copias de seguridad (backups) inmutables y aisladas (air-gapped) para garantizar la restauración rápida ante un ataque de ransomware sin abonar rescates.

### 3. Controles Administrativos
* **Preventivos:** Creación y difusión de políticas estrictas de contraseñas y programas de concientización en ciberseguridad para evitar caídas ante correos de phishing (ingeniería social).
* **Detectivos:** Revisiones periódicas de auditoría de cumplimiento de políticas y auditorías de cuentas de usuarios inactivos o con privilegios elevados.
* **Correctivos:** Procedimientos formales de Respuesta a Incidentes (Incident Response Plan) y planes de continuidad de negocio (BCP).

---

## 🧠 Conclusiones y Lecciones Aprendidas
* La seguridad efectiva no depende de una sola herramienta, sino de la combinación equilibrada de **controles físicos, técnicos y administrativos**.
* La defensa en profundidad evita que una falla humana o técnica (como un correo de phishing o un estudiante obteniendo credenciales) comprometa la totalidad de la infraestructura escolar.
