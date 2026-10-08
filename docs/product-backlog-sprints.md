# Product Backlog y planificación Scrum

**Proyecto:** Sistema de Gestión de Residuos Orgánicos Agroindustriales – Finca Catalina  
**Estado:** Planificación propuesta; el avance real debe actualizarse con evidencias.

## Roles Scrum propuestos
- **Product Owner:** representa a los usuarios y prioriza el valor.
- **Scrum Master:** facilita el proceso y ayuda a resolver impedimentos.
- **Equipo de desarrollo:** diseña, implementa, prueba y documenta el incremento.

En un proyecto individual académico, una persona puede asumir varios roles; no se deben presentar reuniones simuladas como ceremonias reales.

## Product Backlog priorizado

| Prioridad | ID | Historia de usuario | Criterio de aceptación resumido | Estimación inicial |
|---:|---|---|---|---:|
| 1 | PB-01 | Como usuario autorizado, quiero iniciar sesión para acceder según mi rol | Credenciales válidas permiten acceso; inválidas son rechazadas | 5 puntos |
| 2 | PB-02 | Como operario, quiero registrar una recepción de residuos | Campos obligatorios válidos, cantidad positiva y código único | 8 puntos |
| 3 | PB-03 | Como coordinador, quiero consultar recepciones | Búsqueda por código y visualización de datos | 5 puntos |
| 4 | PB-04 | Como responsable, quiero actualizar el estado de recepción | Solo se permiten transiciones válidas y auditadas | 5 puntos |
| 5 | PB-05 | Como coordinador, quiero consultar la trazabilidad de un lote | Historial ordenado por fecha y asociado al lote | 8 puntos |
| 6 | PB-06 | Como encargado, quiero programar rutas de recolección | Origen, destino, fecha y estado consultables | 8 puntos |
| 7 | PB-07 | Como operario, quiero registrar peso y observaciones | Datos válidos asociados al lote y fecha | 5 puntos |
| 8 | PB-08 | Como administrador, quiero generar reportes por periodo | El reporte muestra periodo, fuente y fecha de generación | 8 puntos |
| 9 | PB-09 | Como responsable de calidad, quiero consultar indicadores | Cada indicador tiene fórmula, unidad, periodo y fuente | 5 puntos |
| 10 | PB-10 | Como administrador, quiero gestionar catálogos | Solo usuarios autorizados pueden cambiar valores controlados | 5 puntos |

## Sprint 1 — Registro básico
**Objetivo:** definir y validar el flujo principal de acceso y recepción.
- PB-01: acceso y roles.
- PB-02: formulario de recepción y validaciones.
- PB-03: consulta de registros.
- Actividades transversales: diseño de datos, arquitectura, pruebas y documentación.

## Sprint 2 — Seguimiento y trazabilidad
**Objetivo:** ampliar el registro para seguir los residuos durante el proceso.
- PB-04: estados y registro de cambios.
- PB-05: trazabilidad de lotes.
- PB-06: programación de rutas.
- PB-07: peso y observaciones.
- PB-08 y PB-09: reportes e indicadores, según capacidad y alcance aprobado.

## Eventos y artefactos
- **Planificación:** seleccionar historias según prioridad y capacidad.
- **Daily Scrum:** inspeccionar avance e impedimentos si el equipo realiza esta reunión.
- **Revisión:** demostrar el incremento y recoger comentarios.
- **Retrospectiva:** acordar una mejora de trabajo.
- **Artefactos:** Product Backlog, Sprint Backlog e incremento verificable.

## Definición de terminado (DoD)
Una historia solo se considera terminada cuando sus criterios de aceptación se revisan, las pruebas acordadas se ejecutan, los resultados quedan documentados, el cambio se revisa y la documentación se actualiza.

## Métricas
- Cumplimiento del Sprint = historias aceptadas / historias comprometidas × 100.
- Variación de estimación = (esfuerzo real − esfuerzo estimado) / esfuerzo estimado × 100.
- Registrar datos reales al finalizar cada Sprint. No asignar porcentajes de cumplimiento antes de tener evidencia.
