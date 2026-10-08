# Gestión de riesgos y métricas de calidad

## 1. Matriz consolidada de riesgos
Las probabilidades e impactos son valoraciones iniciales cualitativas. Deben revisarse periódicamente con responsables y evidencias del proyecto.

| ID | Riesgo | Probabilidad | Impacto | Prioridad | Prevención / respuesta | Indicador de seguimiento |
|---|---|---|---|---|---|---|
| R-01 | Pérdida o corrupción de registros | Media | Alto | Alta | Copias de respaldo, control de acceso y prueba de restauración | Último respaldo y restauración verificada |
| R-02 | Registros incompletos o cantidades incorrectas | Alta | Alto | Alta | Validar campos, fecha, unidad y cantidad; mostrar mensajes claros | Porcentaje de registros rechazados por validación |
| R-03 | Conectividad inestable en campo | Alta | Alto | Alta | Mensajes de error y diseño de recuperación; evaluar modo offline si el alcance lo requiere | Operaciones fallidas por conexión |
| R-04 | Acceso no autorizado o exposición de datos | Media | Alto | Alta | Autenticación, permisos por rol, sesiones seguras y no guardar secretos en Git | Incidentes de acceso y revisiones de permisos |
| R-05 | Retraso de actividades o alcance excesivo | Media | Medio | Media | Priorizar backlog, dividir historias y revisar capacidad de Sprint | Historias aceptadas / comprometidas |
| R-06 | Defectos al cambiar estados de recepción o lotes | Media | Alto | Alta | Definir transiciones válidas y pruebas de estados | Pruebas de transición aprobadas / ejecutadas |
| R-07 | Métricas sin datos confiables | Media | Alto | Alta | Definir fuente, fórmula, periodo y responsable; no inventar resultados | Indicadores con fuente y evidencia completas |
| R-08 | Pérdida de trazabilidad entre recepción y despacho | Media | Alto | Alta | Identificadores únicos y eventos con fecha, usuario y lote | Registros con historial completo / registros muestreados |
| R-09 | Dificultad de uso para personal de campo | Media | Medio | Media | Prototipo sencillo, accesibilidad y pruebas con usuarios | Tareas completadas / intentadas |
| R-10 | Inconsistencia entre documentos y repositorio | Media | Medio | Media | Actualizar README, catálogo ECS y auditoría en cada cambio | Elementos del catálogo con versión y ubicación vigentes |

## 2. Calidad: ISO/IEC 25000 y GQM
ISO/IEC 25000 (SQuaRE) ofrece un marco para evaluar requisitos y calidad de sistemas y software. GQM significa Goal–Question–Metric (Objetivo–Pregunta–Métrica) y vincula cada indicador con un objetivo de evaluación.

| Objetivo | Pregunta | Métrica / fórmula | Fuente | Frecuencia |
|---|---|---|---|---|
| Evaluar adecuación funcional | ¿Los casos de prueba cumplen los criterios? | Casos aprobados / casos ejecutados × 100 | Registro de pruebas | Por versión |
| Evaluar integridad de datos | ¿Qué proporción de registros cumple las validaciones? | Registros válidos / registros evaluados × 100 | Datos de prueba y logs | Por versión |
| Evaluar confiabilidad | ¿Cuántas operaciones terminan sin error? | Operaciones correctas / operaciones ejecutadas × 100 | Logs o pruebas controladas | Por periodo |
| Evaluar usabilidad | ¿Qué proporción de tareas completa el usuario? | Tareas completadas / tareas intentadas × 100 | Prueba de usuario | Por ronda |
| Evaluar mantenibilidad | ¿Cuánto tarda un cambio en revisarse e integrarse? | Mediana de tiempo entre apertura y cierre de PR | Historial de GitHub | Mensual |
| Evaluar proceso Scrum | ¿Qué proporción del compromiso se completó? | Historias aceptadas / historias comprometidas × 100 | Backlog y revisión de Sprint | Por Sprint |

## 3. Cuadro de mando inicial
| Indicador | Meta propuesta | Resultado actual | Acción ante incumplimiento |
|---|---:|---|---|
| Casos de prueba aprobados | ≥ 90% antes de liberar | Sin medir | Analizar fallos y repetir pruebas |
| Registros válidos en prueba controlada | ≥ 98% | Sin medir | Revisar reglas de validación |
| Tareas de usuario completadas | ≥ 85% | Sin medir | Ajustar interfaz y volver a probar |
| Cumplimiento de Sprint | ≥ 80% como referencia inicial | Sin medir | Revisar capacidad y estimación |
| Registros con trazabilidad completa | ≥ 95% | Sin medir | Revisar identificadores y eventos |

## 4. Seguimiento
Para cada riesgo se debe registrar responsable, fecha de revisión, cambio de probabilidad/impacto y acción acordada. Para cada métrica se debe conservar el valor observado, el periodo, la fuente de datos y la evidencia. Las metas son objetivos propuestos y no resultados obtenidos.

El plan de casos y el registro de ejecución se encuentran en [pruebas-y-metricas.md](pruebas-y-metricas.md).
