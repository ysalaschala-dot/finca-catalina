# Plan de pruebas y registro de métricas

**Estado inicial:** casos propuestos; ejecución pendiente de evidencias verificables. No se han inventado resultados.

## 1. Casos de prueba

| ID | Caso | Procedimiento | Resultado esperado | Estado inicial |
|---|---|---|---|---|
| CP-01 | Acceso válido | Ingresar credenciales de prueba válidas | Acceso conforme al rol | Pendiente |
| CP-02 | Acceso inválido | Ingresar credenciales incorrectas | Se deniega el acceso y aparece un mensaje claro | Pendiente |
| CP-03 | Recepción válida | Completar los campos con datos válidos | Registro con código único | Pendiente |
| CP-04 | Campo obligatorio | Omitir un campo requerido | No se guarda y se informa qué corregir | Pendiente |
| CP-05 | Cantidad no válida | Ingresar cero, negativo o texto | Se rechaza la cantidad | Pendiente |
| CP-06 | Fecha no válida | Ingresar fecha/hora incorrecta | Se rechaza el dato | Pendiente |
| CP-07 | Código duplicado | Intentar guardar un código repetido en entorno de prueba | Se impide el duplicado | Pendiente |
| CP-08 | Estado no permitido | Solicitar transición inválida | Se rechaza y se conserva el estado | Pendiente |
| CP-09 | Permisos | Ejecutar función con rol no autorizado | Acción bloqueada | Pendiente |
| CP-10 | Trazabilidad | Consultar lote existente e inexistente | Historial correcto o mensaje de no encontrado | Pendiente |
| CP-11 | Reporte | Consultar periodo con datos de prueba conocidos | Cálculo coincide con datos fuente | Pendiente |
| CP-12 | Restauración | Restaurar respaldo en ambiente de prueba | Datos recuperados coinciden con el respaldo | Pendiente |

## 2. Registro de ejecución
Completar solo después de ejecutar cada prueba.

| ID | Fecha | Ambiente/versión | Resultado real | Evidencia | Incidencia |
|---|---|---|---|---|---|
| CP-01 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |
| CP-02 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |
| CP-03 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |
| CP-04 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |
| CP-05 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |
| CP-06 | Pendiente | Pendiente | No ejecutado | Pendiente | Pendiente |

## 3. Métricas propuestas con enfoque GQM
GQM significa Goal–Question–Metric (Objetivo–Pregunta–Métrica). Las fórmulas se deben calcular con datos reales.

| Objetivo | Pregunta | Métrica | Fuente |
|---|---|---|---|
| Adecuación funcional | ¿Qué proporción de pruebas cumple? | Pruebas aprobadas / pruebas ejecutadas × 100 | Registro de pruebas |
| Control de defectos | ¿Qué defectos se detectan antes de liberar? | Defectos previos a liberación / defectos confirmados × 100 | Incidencias |
| Confiabilidad | ¿Qué proporción de operaciones termina sin error? | Operaciones correctas / operaciones ejecutadas × 100 | Logs o pruebas controladas |
| Usabilidad | ¿Qué tareas completan los usuarios? | Tareas completadas / tareas intentadas × 100 | Prueba con usuarios |
| Mantenibilidad | ¿Cuánto tarda un cambio? | Mediana de tiempo entre apertura y cierre de cambios | Issues y PR |
| Planificación | ¿Se completó el Sprint? | Historias aceptadas / historias comprometidas × 100 | Backlog y revisión |

## 4. Tablero inicial
| Indicador | Meta propuesta | Resultado medido |
|---|---:|---|
| Pruebas aprobadas antes de liberar | ≥ 90% | Sin medir |
| Registros válidos en prueba controlada | ≥ 98% | Sin medir |
| Tareas de usuario completadas | ≥ 85% | Sin medir |
| Cumplimiento del Sprint | ≥ 80% como referencia inicial | Sin medir |

Las metas son objetivos propuestos, no resultados obtenidos. No cambiar “Sin medir” hasta ejecutar pruebas y guardar evidencia.
